# Leaderboard
The ultimate challenge of automated farming is to play through the game automatically as fast as possible.

Calling `timed_reset()` will save the game, reset all unlocks and upgrades that aren't about programming, and start the leaderboard timer.

You keep all language features like `while, if, for`, variables, operators and senses.
You also get to keep costs and auto unlocks so you can fully automate playing through the game.

If the program execution stops, the run is aborted.
The run is finished when the execution calls `timed_reset()` again. 
You do not need to have everything unlocked, just try to unlock `Unlocks.Leaderboard` and call `timed_reset()` as fast as possible.

After the run is finished or aborted the save from before the run is loaded again.

While the timer is running you have the option to speed up the time so you don't have to wait so long.


Remember that you can use `num_unlocked(unlock) > 0` to check if something is unlocked and you can use `get_cost()` on your unlocks to see what they cost so you can automatically farm the right items.