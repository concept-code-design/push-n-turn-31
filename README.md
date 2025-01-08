# push-n-turn-31

Simple MIDI controller with three (keyboard style) keys and a rotary encoder (with push button). 

The keys can be used in note mode or ControlChange mode. The encoder sends CC codes.
The notes and CC codes are programmable. 
Each key has an RGB indicator light.
The controller has a USB type-C connector and produces USBMidi codes. Works with MacOS, Linux, Windows.  

Configuration/mode switching
| key combo | feedback | description
| ------------------------------------- | ----------------------- | --------------------------- |
| press left and right key (2 secs)| 3 x yellow | switches between note mode/CC mode
| press enc + right key (2 secs) | 3 x deep purple | enter programming mode
| rotate encoder | dark blue green | select key to program
| press enc (in programming mode) | aqua | exit programming mode
| 

Normal operation
| mode | feedback | description
| -------- | ------------------ | ---------------------
| **note mode** | |
| press any key | spring green | send note on
| release any key | | send note off
| turn encoder | light 3 will show position (from green..red) for .5 sec | send CC + current value
| press encoder | light 3 will flash for .5 sec | send CC + 127
| **CC mode** | |
| press any key | blue/off | toggle between on (CC key 127) and off (CC key 0)
| turn encoder | light 3 will show position (from green..red) for .5 sec | send CC + current value
| press encoder | light 3 will flash for .5 sec | toggle between on (CC key 127) and off (CC key 0)

**Programming key-note combos**
Once in programming mode, select the key to program. The selected key's light will turn dark blue green. Use your DAW or keyboard or whatever to send the desired note to the controller. If the controller registers the note, it will send it back to the host after 0.5 sec and turn the indication light blue. Rinse and repeat. Onmce done press the encoder button. The controller will return to note mode.
