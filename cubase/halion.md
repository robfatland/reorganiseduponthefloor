# Halion sample editor


[YouTube One Man And His Songs video](https://youtu.be/AJJIldGPX7o?si=AfolDtTUFjlRS59E)


## Part 1: Sample in Cubase > Halion Instrument configuration > save > trigger


- Create an audio track, set up a mic, record a short event to be the basis of an Instrument track
    - This example presumes the event is 'turn left' sung at some pitch (F2)
- Edit the event in the track with VariAudio. **Bounce** the event to remove extra baggage
- Can run Halion as standalone or start it by adding an Instrument track
    - Halion is configured as a rectangle of panels, the panels often tabbed
    - The main idea is to use upper right dropdown or right click to manipulate these panels
        - A panel split brings up a menu of 'what is it?' for the new panel
    - Halion standalone: From the upper left choose the Screenset chooser icon: Advanced configuration
    - Halion from Add Instrument Track: Choose the Sample configuration
        - For consistency with standalone: 
            - Program Tree panel at right: rt-click: choose `split --` and add a Program Table
            - Remove the Init program from the Slot Rack and the Program Table
    - Panels should now include the Program Table, Program Tree, Slot Rack, Workbench (center), Master (top left)
        - There are also some keyboard panels at the lower left
- Program Table at lower right: Drag Program 1 to first Slot Rack slot and rename it 'turn left'
- Program Tree: Click the sine wave icon and add a Sample Zone: yellow icon means empty
- Workbench select EDIT in the top row; select SAMPLE in the second row
    - Drag in the sample from Cubase. Zone 1 icon becomes blue.
- Save this: Floppy disk icon in the Master, upper left
- Create a MIDI event with a couple 'turn left' notes and notice the default behavior
    - Create a MIDI note: Its duration controls length of playback
    - MIDI controls pitch; note duration becomes longer/shorter in support of pitch
    - MIDI note start < Transport < MIDI note end: Play iniiates the MIDI note from start (not middle)
    - C3 plays sample at recorded pitch
    - The full keyboard from C-2 t o C7 is available
- Close the editor and re-open it: Verify Halion starts in pretty much the same configuration
- In Halion Master select the folder icon for 'Load Multi-Program'
    - The interface filter is Stupid: Click on Factory to De-select, make sure User is selected: Should see 'turn left'.
    - I have no idea where User stuff is stowed
- Stop and re-start Cubase to verify everything is still there; instrument should again open in the same configuration
- Optional: Check that the Instrument track can monitor a physical keyboard and play polyphonic samples at all pitches
- Optional: Send the Instrument track to a Reverb FX track


## Part 2: Panels and terms

  
- Program Table is the on deck circle 
- Slot rack is batter(s) up: Qty 4 x 16 = 64
- Program tree: Sine wave symbol to add Zones; here chosing Sample
- Workbench
    - Sample Editor is one of many types of editors. 
        - Here: Sample S is a Mono recording isolated on a track in Cubase 
    - Upper bar select the EDIT button
        - Investigate LOAD/REC...
    - Sub-menu includes SOUND, ZONE, MIDI MOD, MAPPING, SAMPLE, WAVETABLE
        - ZONE and SAMPLE are what I am interested in; SAMPLE is used for the drag-and-drop
- Terms
    - PRESET is the entire sound entity: 1 or more PROGRAMS (hence 'multi-program')
    - PROGRAM is one or more LAYERS 
    - LAYER is a CONTAINER (bucket): A basic building block: Includes a Zone and a Bus and possibly/often a MIDI Controller
    - ZONE: Main element of the LAYER: 5 Types of Basic Sound Source: Synth, Sample, Granular, Organ, Wavetable
        - A Zone with a yellow icon is empty


## Part 3: Modifying the Instrument by working with the Sample Editor


- Review the default behavior of MIDI triggers in an Instrument Track: See part 1 above
    - Features to manage
        - Keyboard note accurately reflects playback pitch
            - EDIT > MAPPING > Modify Root key (in this case to F2)
        - Fixed-length playback: Does not vary with trigger pitch
- EDIT > SAMPLE > up-arrow icon is Normalize to dB value shown to the right
