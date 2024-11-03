# Cactus
Cacti can be grown on soil from cactus seeds.

They have an odd sense of community.

When you harvest a cactus all cacti on the field are harvested.
The number of cactus items dropped per cactus is equal to the world size as returned by `get_world_size()`.

A cactus only drops cactus items when harvested if it's in sorted order. 
A cactus is considered to be in sorted order if there is a smaller or equal cactus to the `South` and to the `West` and a larger or equal cactus to the `North` and to the `East`.
Essentially the cacti must be sorted in increasing x and y directions for them to drop anything.

If a cactus is at the edge of the field, only the existing neighboring fields need to be correct for it to be sorted.

The size of a cactus can be measured with `measure()`. 
It is always one of these numbers: `0,1,2,3,4,5,6,7,8,9`.

You can also pass a direction into `measure(dir)` to measure the neighboring tile in that direction of the drone.

You can swap a cactus with its neighbor in any direction using the `swap()` command.
`swap(direction)` swaps the object under the drone with the object one tile in the `direction` of the drone.

<spoiler=show hint 1>
If every column and every row of the field is sorted then all plants are in sorted order.
</spoiler>
<spoiler=show hint 1>
You get rewarded for every cactus that is in sorted order. If some cacti are in sorted order you will already get some of the reward. You don't have to sort 100%.</spoiler>