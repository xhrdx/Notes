# Thu 6 Nov

Take note that Tomasule takes 5 and not 4 steps, figure out why. (mentioned in today's slides)

## ROB/Tomasulo

1. Allocating a spot in the reorder buffer (ROB) for add F4 we also dispatch it to the reservation stations the thing with 1,2,3 rows (ADDD 2.0 0.0 ROB0) and we add the allocated entry F4->(4.0 ROB0)

Floating point operations take a long time so it's usually pipeline so that we don't have to a big cycle time, plus it's cheap to throw in there some intermediate pipeline registers.

floating point adder is more commplex than an FP multiplier

2. We do the same thing with the MULD but it goes at the reservation stations above the FP mult's and so on and so forth.

When the ADDD 2.0 0.0 ROB0 gets calculated do we free the corresponding reservation station tuple?


The H on the top right means that this instruction is at the head of the queue

On the 5th cycle, the MULD was listening for the F4 so when it was available it got the value of it...


MIPS/ROB

The (Integer/FP/etc) Queue is like a reservation station
