The mouseswitch of choice in these projects is the Omron D2LS, available from any electronics distributer for about $2.5CAD each. I use the blue (60gf) for everything, but be forewarned that most gamers I've spoken to say this is uncomfortably light for them; consider ordering a small handful of both the 60 and 120s if you're unsure, but I feel 60 is adequate.

# Project 1: Backpaddle and Insert
Slide-in insert for GCC that allows custom hardware to be mounted to the back. The files for "backpaddle-neo" are my latest revision of a mouseclick back-paddle that can be wired up to any desired input. This is sized and oriented for my hand, and on my hand this is lined up to be comfortably input with my middle finger (this one 🖕). To attach the backpaddle to the backplate, I used 4.5mm M1.4 screws and nuts from a watch repair kit. 
The current revision has "shotgun" screw holes so people can design other modular attachments with differently oriented screws if needed; the arrangement of the shotgun holes is contained in the .dxf file. 
On an FDM printer, make sure to rotate the model so that the mounting side (the big flat part) is aligned with the buildplate. 
The included file is for the right hand; the STL can be mirrored in your slicer program to obtain a "left hand" paddle.

# Project 2: Double Mouseclick Shoulder
Self-explanatory-- Two buttons in one shoulder-slider slot. I use the "lower" button for C stick up. This revision of the button shapes is significantly better than any other revision I've tried in terms of not jamming against each other, not lean/squeeze-jamming against the GCC shell, and not actuating button 2 when button 1 is bumped off-axis. 

## Notes on hooking up switches to "extra inputs" on GCC.
- Making these extra switches input C-up/C-down on OEM GCC seems pretty challenging. Consider consulting the schematic for rana labs' "C-pad" for a reasonable discrete-component electrical approach. I think you need diodes and stuff.
- Making these extra switches input C-up/C-down on PhobGCC has different annoyances depending on revision. On PhobGCC 1.x finding extra pins to hook onto is hard, but writing custom firmware is very easy; on PhobGCC 2.x there are "extra GPIO" pins routed that make the hardware part trivial, but it's somewhat harder to write/build custom firmware. 
- Basically every competitive Smash Bros Melee Ruleset agrees that "extra buttons" (as in, copies of inputs) are not acceptable-- e.g. if you wire up your back-paddle to C-stick-down, you must also disable C-stick-down on the C-stick. Doing this in Phob firmware is the easiest method.
