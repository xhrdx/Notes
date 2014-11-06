# Thu 6 Nov

Take note that Tomasule takes 5 and not 4 steps, figure out why. (mentioned in today's slides)

## ROB/Tomasulo

1. Allocating a spot in the reorder buffer (ROB) for add F4 we also dispatch it to the reservation stations the thing with 1,2,3 rows (ADDD 2.0 0.0 ROB0) and we add the F4->(4.0 ROB0)

Floating point operations take a long time so it's usually pipeline so that we don't have to a big cycle time