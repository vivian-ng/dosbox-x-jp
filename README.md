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
