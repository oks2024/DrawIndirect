This small project allow to test the performances of the drawIndirect function.

I made this because I noticed that an indirect draw call was slower than a regular one with the same parameters on my computer/graphic card.

It's just a tutorial from the directX samples modified so it can draw a large number of vertices and output the timing in the console.

You can comment the lines 426/427 to use a draw command or the other.
You can change the number of vertices to draw by editing the line 44.

On my AMD R9 290 drivers 14.9 for 900 000 vertices:

DrawInstanced: 0.31ms
DrawInstancedIndirect: 0.42ms

For 9 000 000 vertices:

DrawInstanced: 0.31ms
DrawInstancedIndirect: 0.42ms

On my NVIDIA GT 630m:

For 900 000 vertices:

DrawInstanced:2.72ms
DrawInstancedIndirect: 2.72ms

For 9 000 000 vertices:

DrawInstanced:26.87ms
DrawInstancedIndirect: 26.87ms

I also tried on a GTX780 and there is no difference between DrawInstanced and DrawInstancedIndirect.

If you haves a clue on why the drawIndirect is slower on my AMD card I would be happy to hear it. Maybe something is wrong on my code, or on my computer, if you experience the same issue would be happy to add your results.
