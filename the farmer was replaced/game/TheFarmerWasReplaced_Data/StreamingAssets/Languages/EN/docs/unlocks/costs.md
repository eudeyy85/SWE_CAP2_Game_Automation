# Costs
Any cost can be represented as a dictionary that maps items to numbers.

The `get_cost()` function returns such a dictionary. It returns the price to buy an item using the `trade()` function, the seed required to plant a plant, or the cost of an unlock.

`get_cost(Items.Pumpkin_Seed)`
returns `{Items.Carrot:1}`

`get_cost(Entities.Pumpkin)`
returns `{Items.Pumpkin_Seed:1}`

`get_cost(Unlocks.Loops)`
returns `{Items.Hay:5}`

For upgrades that are already at the max level the `get_cost()` will return `None`.

It can be used like this:
`cost = get_cost(something)
for item in cost:
	amount_of_this_item_needed = cost[item]`
