# Flight Risk

I initially tried to solve this challenge and spent a lot of time looking in the wrong place. On seeing the writeups i understood what exactly had to be done and it seemed fairly simple.

I knew i had to alter the game files somehow but i didn't know where or what to alter. 
But i was fairly close in my approach, the execution just didn't work out. The solution was to alter the game files on IDA which was basically spawning the missile.
So to get the flag, after opening up the game on IDA, the missile and terraingenerator classes were modified and basically set to 0. 
#
