# Watering
Plants grow faster when they are watered. The ground has a water level ranging from `0` to `1`.
The function `get_water()` returns the water level of the ground it is over.

The growth speed of a plant growing on tilled soil grows linearly from 1x speed at water level 0 to 5x speed at water level 1.
Watering only affects plants growing on tilled soil. It doesn't have any effect on plants growing on turf.

Soil dries up over time: The water loses 1% of it's current water every now and then. Keeping the water level high will consume much more water than keeping it low.

You can use water tanks to water your plants. You can purchase empty tanks with wood using `trade(Items.Empty_Tank)`

A tank can hold `0.25` water.

Tanks fill up automatically. The fill rate is `0.5`% of the number of empty tanks per second. So if you have `100` empty tanks one of them will fill every `2` seconds.

Call `use_item(Items.Water_Tank)` over any ground to empty a tank and water the ground.
