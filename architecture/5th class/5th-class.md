# 5th Class - Thu 16 Oct

## Since misprediction penalty is larger, we first focus on branch (direction) prediction

* Whether or not the processor should guess that the branch is taken (takes into account the taken vs not taken ratio)
Extra programming burden optimization turned on doesn't work the same way as the non optimized way

## A note on prediction/misprediction rates


From 96%->98% big deal right you went from 96 to 98... Yes however the mispredict rate is half of what it was so it's twice as good the brances that are predicted correctly are 2 times more...


## Dynamic Branch Prediction – Track Changing Per-Branch Behavior 

with one bit we lose precision when you have loops. The last time we exited the loop so the first time we're gonna predict that we're gonna exit it again...

Let's use a two bit