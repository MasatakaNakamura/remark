To have a start page listing all .html files in your remark file, create a file called index.php with the following code:

```
<?php
echo "Here are our files:</br></br>";
$path = ".";
$dh = opendir($path);
$i=1;
while (($file = readdir($dh)) !== false) {
    if($file != "." && $file != ".." && $file != "index.php" && $file != ".htaccess" && $file != "error_log" && $file != "cgi-bin" && strtolower(substr($file, strrpos($file, '.') + 1)) == 'html') {
        echo "<a href='$path/$file'>$file</a><br /><br />";
        $i++;
    }
}
closedir($dh);
?> 
```