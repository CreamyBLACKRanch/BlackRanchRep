# schlagenheim
Flag: `citadel{8lackM1D1wa5c00l}`

### Solve
The `.wav` file given was corrupt<br>
We opened it in an hex editor to see the bytes of the file<br>
Some bytes say `M1D1`, this gives us a clue that the file should be MIDI (The word`mid` was also given in the description, which was another clue)
<br>We changed `M1D1` to `MThd` as the file is supposed to be a MIDI file.<br>
We used the Audacity applicaiton to visualize the file, and then we saw the flag.