# dosbox-x-jp
Additional files to run DOSBox-X with JP106 Japanese keyboard

Put the following files into your DOSBox-X directory, run dosbox-x and it should work.

jp.kl<br/>
mapper-jp106.map<br />
dosbox-jp.conf<br />

You can find DOSBox-X here:<br />
https://github.com/joncampbell123/dosbox-x

To run dosbox-x with this configuration, you need to use<br/>
dosbox-x -conf dosbox-x-jp.conf

Notes:

jp.kl is the keyboard layout file, which I found here:<br />
(https://www.wizforest.com/trash/dosbox/dosbox-r3850-jp.rar)<br /> 
mapper-jp106.map is the mapper file created after running dosbox-x and adding in the keyboard mapping for 
backslash "\\" and the yen character. dosbox-x-jp.conf has been updated to load mapper-jp106.map on start and 
run with "jp" keyboard layout.

2018/12/19
----------
I found an easier way to get JP106 keyboards to work with DOSBox 0.74. As long as DOSBox is executed in the directory containing jp.kl and the config file has the correct mapper and keyboardlayout defined, it works. You do not need DOSBox-X. Note, however, that without DOSBox-X, certain keys on JP106 keyboards, like the yen key and backslash key, cannot be mapped. Still, this is a quick and dirty way to at least get JP106 keyboard working (partly) in DOSBox 0.74.<br/>
<br/>
Example script:
```
#!/bin/bash
cd ~/dosbox-x-jp
dosbox -conf dosbox-0.74jp.conf
```
This assumes this repository is cloned to the user's home directory under the directory name `dosbox-x-jp`, and the config file with the jp keymapper and keyboardlayout defined is `dosbox-0.74jp.conf`.<br/>
<br/>
For Windows, it can be a batch file (.BAT)
```
#!/bin/bash
cd %userprofile%\dosbox-x-jp
dosbox -conf dosbox-0.74jp.conf
```

Then, all you need to do is to put the script in the path (for Linux) or create a shortcut to the .BAT file (for Windows).
