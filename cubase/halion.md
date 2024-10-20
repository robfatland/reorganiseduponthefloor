# Halion sample editor


[YouTube One Man And His Songs video](https://youtu.be/AJJIldGPX7o?si=AfolDtTUFjlRS59E)

## Preamble
- The tune **Favor** features multiple instruments; however with duration proportional to pitch
- Overview is to first set up some audio clip (possibly use VariAudio) and then assign it to a Halion instrument
    - Remember to use 'Bounce' like a print/render function that detaches the signal from its source copy
- One man and his songs link above is to the Steinberg Halion 6 Tutorial 'Ep.13: The Sample Editor'



## Part 1: Sample in Cubase > Halion Instrument configuration > save > trigger


- Create an audio track, set up a mic, record a short event to be the basis of an Instrument track
    - This example presumes the event is 'turn left' sung at some pitch (F2)
- Edit the event in the track with VariAudio. **Bounce** the event to remove extra baggage
- Can run Halion as standalone or from within Cubase by adding an Instrument track
    - Default Halion is configured as a rectangle of panels and these panels are often tabbed
        - Main idea: Upper right dropdown or right click to manipulate these panels
        - A panel split brings up a menu of 'what is it?' for the new panel
    - Halion as standalone: From the upper left choose the Screenset chooser icon: Advanced configuration
    - Halion as Cubase Add Instrument Track: Choose the Sample Instrument configuration
        - To make this consistent with the standalone option... 
            - ...on the Program Tree panel (rt): upper rt menu: `split --`, add a Program Table
            - Remove the Init program from the Slot Rack and the Program Table
    - Panels should now include the Program Table, Program Tree, Slot Rack, Workbench (center), Master (top left)
        - Also some keyboard panels at the lower left
        - Saved this as `blank_single_instrument`
- Open issue: We seem to be creating a Multi-Instrument; there is not really a Mono-Instrument in contrast; kun?
- Program Table at lower right: Drag Program 1 to first Slot Rack slot and rename it 'turn left'
- Program Tree at upper right: Click sine wave icon, add Sample Zone: yellow icon 'Zone 1' is empty
- Workbench select EDIT in the top row; select SAMPLE in the second row
    - Drag in the sample from Cubase. Zone 1 icon becomes white, Zone 1 text has light blue background.
- Save in Master panel
    - There are two save options, both with floppy disk icons, adjacent
    - Left floppy disk icon is "Save Multi-program as..." (resulting dialog lists earlier efforts as well)
    - Right floppy disk icon is "Export Multi-program as VST3 Preset with Files"
    - Open issue: What do these saves respectively accomplish?
- In the Instrument track use the pencil to create an editable MIDI event and double click to open in Editor
    - Use the pencil to create a couple of MIDI 'turn left' notes; notice the default behavior
        - Duration of the MIDI note controls length of playback, pitch is pitch
        - The natural duration of a note goes inversely with pitch 
    - MIDI note start < Transport < MIDI note end: Play initiates the MIDI note from start (not middle)
    - Open issue: How is the 'plays at recorded pitch' key chosen? Always C3? VariAudio? How to change?
    - Full keyboard is C-2 through C7
- Close the editor in Cubase and re-open it: Verify the Instrument track looks the same
- Close Halion and re-open it: Verify it is in pretty much the same configuration
- In the Halion Master panel select the folder icon 'Load Multi-Program'
    - The interface filter is overloaded by default:
        - Click on Factory to De-select it, ensure User is selected: Should see 'turn left' and other saved Multi-Instruments
    - I believe this is stored in the Project/Audio folder
- Stop and re-start Cubase to verify everything is still there; instrument should again open in the same configuration
- Check that the Instrument track can monitor a physical keyboard and play polyphonic samples at all pitches
- Send the Instrument track to a Reverb FX track


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
        - To do: Keyboard note accurately reflects playback pitch
            - Solution: EDIT > MAPPING > Modify Root key (in this case to F2)
        - To do: Fixed-length playback duration, pitch independent
            - Solution: None yet
- EDIT > ZONE has some useful features but is mostly replicated by EDIT > SAMPLE
    - As a result: Mostly leave this alone in favor of...
- EDIT > SAMPLE > up-arrow icon is Normalize to dB value shown to the right
    - There are three sets of range markers: Sample range (S, S), Loop range (L, L) and Release (R, R)
        - Visibility is tied to playback mode in EDIT > SAMPLE editor LOOP page (tab at lower left)
- Topic: Working with the Wavetable
- Topic: Working with envelopes
- Topic: Multiple Zones e.g. turn-left and turn-right
- Topic: Building an Instrument by combining adjacent small pitch ranges
