# Sunflowers
Sunflowers collect the power of the sun. You can harvest that power. 

Planting them works exactly the same way as planting carrots, except you have to buy sunflower seeds instead of carrot seeds. 

However, when you harvest a sunflower, the power of all the sunflowers on the farm flows together into the harvested plant. 
Thus, harvesting a sunflower yields power equal to the square root of the number of sunflowers on the farm.
Only one of the sunflowers with the most petals can handle this.
If you harvest a sunflower that doesn't have the most petals of all the sunflowers on the farm the power will destroy all the sunflowers on the farm.

`measure()` returns the number of petals of the sunflower under the drone.
Sunflowers have at least `7` and at most `15` petals.
They can be measured before they are fully grown.

Several sunflowers can have the same number of petals so there can also be several sunflowers with the largest number of petals. In this case, it doesn't matter which one of them you harvest.

As long as you have power the drone will use it to run twice as fast. 
It consumes 1 power every 30 actions (like moves, harvests, plants...)
Executing other code statements can also use power but a lot less than drone actions.

In general, everything that is sped up by speed upgrades is also sped up by power.
Anything sped up by power also uses power proportional to the time it takes to execute it, ignoring speed upgrades.
