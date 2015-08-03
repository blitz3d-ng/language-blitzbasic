# language-blitzmax package
A Conversion of the BlitzMax TextMate Bundle by nilium (https://github.com/nilium)<br/>
Original project here: https://github.com/nilium/blitzmax.tmbundle<br/>
The original README is kept as README_old.textile<br/>
<br/>
## Manual Installation
1. Install Atom Editor from [atom.io](https://atom.io)
2. Download [repository as .zip](https://github.com/terramultimedia/language-blitzmax/archive/master.zip) and extract *language-blitzmax* - Folder into packages on your machine.<br/>
**Mac OS X:** */Users/username/.atom/packages/*<br/>
**Win** *C:\Users\username\.atom\packages\*<br/>
3. Give feedback and fork it to make it better :D

## Using build Package with BlitzMax
- Using build Package to build Application inside Atom
- runs "bmk"  
- Error Matching moves Coursor to line, where compiling error occured

###Temporary solution:<br/>
1. Install Package: "build" (by noseglide)<br/>
2. Create a file named ".atom-build.json" in your project-root folder and copy&paste following content:<br/>
(You may have to modify the path to your BlitzMax installtion to make it work on your machine)<br/>
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
3. When hitting cmd+alt+b / crtl+alt+b (win) you bmx should be build as an console app, cmd+alt+g as an gui app (see keymap statement in file above)

##Your help needed
Feel free to modify these files and make this package better!<br/> But please: create a pull request etc. to let everybody profitate by the enhancements!
