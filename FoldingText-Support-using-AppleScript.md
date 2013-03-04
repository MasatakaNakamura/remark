This AppleScript will convert a [FoldingText](http://www.foldingtext.com/) outline into a Remark presentation. If stored in the FoldingText "Scripts Folder" it can be accessed by FT's keyboard commands. This script is designed to produce an HTML presentation which differs from the HTML in the README file in two ways: 

1. It is designed for a locally stored `remark.min.js file`. If you wish to pull the online version instead, replace `remark.min.js file` with `https://github.com/downloads/gnab/remark/remark-0.4.4.min.js`

2. It uses an external CSS file, so as to avoid having to code the CSS in AppleScript

The script will start a new slide at every new H1, assuming H1 is marked with a single `#`. This makes it easier to use FoldingText, which can collapse or zoom each slide.

Whenever the FT is updated you can quickly update the Remark HTML by running the script again, it will write-over the previous version. 

> Note, however, that this script cannot (yet) handle Remark's Markdown extensions for slide "name", "class", or "template" as these have to go before the slide division and the script starts a new slide at every `#`. If you have an idea for an improvement to this script, please leave a comment in [the FoldingText Support thread](http://support.foldingtext.com/discussions/questions/357-script-to-generate-remark-formatted-html-file-form-foldingtext) about this script.

```
to searchReplace(thisText, searchTerm, replacement)
    set AppleScript's text item delimiters to searchTerm
    set thisText to thisText's text items
    set AppleScript's text item delimiters to replacement
    set thisText to "" & thisText
    set AppleScript's text item delimiters to {""}
    return thisText
end searchReplace

on write_to_file(this_data, target_file, append_data) -- (string, file path as string, boolean)
    try
        set the target_file to the target_file as text
        set the open_target_file to ¬
            open for access file target_file with write permission
        if append_data is false then ¬
            set eof of the open_target_file to 0
        write this_data to the open_target_file starting at eof as «class utf8»
        close access the open_target_file
        return true
    on error
        try
            close access file target_file
        end try
        return false
    end try
end write_to_file


tell front document of application "FoldingText"
    set thisText to my searchReplace(read text, "
# ", "
---
# ")
    
    set finalText to "<!DOCTYPE html>
<html>
    <head>
    <title>Title</title>
    <meta http-equiv=\"Content-Type\" content=\"text/html; charset=UTF-8\"/>
    <script src=\"remark-min.js\" type=\"text/javascript\"></script>
<link rel=\"stylesheet\" type=\"text/css\" href=\"remark.css\" />
    </head>
    <body>
        <textarea id=\"source\">" & thisText & "</textarea>
        <div id=\"slideshow\"></div>
    </body>
</html>
"
    
    tell front document of application "FoldingText"
        set thedocument to file of front document of application "FoldingText"
        set newPath to ((thedocument as string) & ".html")
    end tell
    
    my write_to_file(finalText, newPath, false)
    
    
    
end tell
```