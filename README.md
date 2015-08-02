# language-blitzmax package
A Conversion of the BlitzMax TextMate Bundle by nilium (https://github.com/nilium)<br/>
Original project here: https://github.com/nilium/blitzmax.tmbundle<br/>
The original README is kept as README_old.textile<br/>
<br/>
## Manual Installation
1. Install Atom Editor
2. Download repository .zip and extract content to your packages folder.<br/>
**Mac OS X:** */Users/username/.atom/packages/language-blitzmax/*

## Using build Package with BlitzMax
Temporary solution:<br/>
1. Install Package: "build" (by noseglide)<br/>
2. Create a file named ".atom-build.json" in your project-root folder and copy&paste following content:<br/>
<pre>{
  "cmd": "/Applications/BlitzMax/bin/bmk makeapp {FILE_ACTIVE_NAME}",
  "cwd": "{PROJECT_PATH}",
  "errorMatch": "\\[(?<file>[^\\.]+.bmx);(?<line>\\d+);(?<col>\\d+)\\]",
  "targets": {
    "GUI Application": {
      "cmd": "/Applications/BlitzMax/bin/bmk makeapp -t gui {FILE_ACTIVE}",
      "keymap": "cmd-alt-g"
    }
  }
}</pre>
