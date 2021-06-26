# basicSoundGrid

Creates a grid of cells in the browser and links them each to sound files. User selects patterns to play sequences.



To load a grid of sounds into the grid interface, just edit the "config" section at the top of the gridApp.html file. Set rows, cols, IOI (inter-onset interval), and the string providing a path to your files.

Your file names must include info that  the [row,col] grid locations map to in order to play them.  The formulas inside the string template ${} use the variables row and col to do the mapping. For example:

The data-filestring: 

data-file2string="`gridAppFiles/demoSndDir/test_2D4pt_d1.${2*col}_d0.${2*row}_v.0.wav`"

will map the grid location row 1, col 3 to play

gridAppFiles/demoSndDir/test_2D4pt_d1.6_d0.2_v.0.wav

and row 2, col 3 to play

gridAppFiles/demoSndDir/test_2D4pt_d1.6_d0.4_v.0.wav

