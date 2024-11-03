# Carrots
Before you can plant carrots with `plant(Entities.Carrots)`, you have to do two new things. First, carrots can only grow on tilled soil. To till the soil, simply call `till()`. Calling `till()` again will change it back to `Grounds.Turf`.

The second new feature is that carrots need seeds to grow. You can buy carrot seeds with the new `trade()` function.
You have to pass an item type to `trade()` like this: `trade(Items.Carrot_Seed)`

If the item can be bought, then it will be bought with this.

You can see the cost of any item in its tooltip. The tooltip appears when you mouse over the item itself or the item name in the code.