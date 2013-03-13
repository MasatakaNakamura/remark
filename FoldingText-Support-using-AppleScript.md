This AppleScript will convert a [FoldingText](http://www.foldingtext.com/) outline into a Remark presentation. If stored in the FoldingText "Scripts Folder" it can be accessed by FT's keyboard commands. This script is designed to produce an HTML presentation which differs from the HTML in the README file in two ways: 

1. It is designed for a locally stored `remark.min.js file`. If you wish to pull the online version instead, replace `remark.min.js file` with `https://github.com/downloads/gnab/remark/remark-0.4.4.min.js`

2. It uses an external CSS file, so as to avoid having to code the CSS in AppleScript

The script will start a new slide at every new H1, assuming H1 is marked with a single `#`. This makes it easier to use FoldingText, which can collapse or zoom each slide.

Whenever the FT is updated you can quickly update the Remark HTML by running the script again, it will write-over the previous version. 

> Note, however, that this script cannot (yet) handle Remark's Markdown extensions for slide "name", "class", or "template" as these have to go before the slide division and the script starts a new slide at every `#`. If you have an idea for an improvement to this script, please leave a comment in [the FoldingText Support thread](http://support.foldingtext.com/discussions/questions/357-script-to-generate-remark-formatted-html-file-form-foldingtext) about this script.

Because the script doesn't display properly in this wiki, I've moved it to Gist:

[FoldingText to Remark AppleScript](https://gist.github.com/kerim/5151560)