# Dinosaurs
Dinosaurs are ancient, majestic creatures that can be farmed for ancient bones.

To get dinosaurs you have to trade eggs and use them with `use_item(Items.Egg)`.

Dinosaurs like to move. From time to time, the dinosaur will swap with a random neighbor.
This swap works just like calling `swap(direction)` manually except that it happens randomly from time to time.

Dinosaurs can be harvested for bones using the `harvest()` command.
There are 4 different types of dinosaurs. 
Harvesting a Dinosaur will also harvest all adjacent Dinosaurs of the same type, so an entire connected group of Dinosaurs will be harvested at once.

The type of a dinosaur can be measured with `measure()`. This will return a unique number for each type of dinosaur.

Remember that you can also pass a direction into measure to measure an entity next to the drone.
`measure(North)` for example will measure the entity to the north of the drone.

The number of bones you get depends on the size of the group of dinosaurs you harvest. Harvesting groups up to 4 will drop bones equal to the square of the group size. Groups of size 4 or larger drop bones equal to 4 times the group size.

Thus, the number of bones per Dinosaur increases with group size up to size 4, and then remains constant.
For optimal efficiency, you always want to harvest groups of size 4 or larger.

Groups also wrap around the side of the farm. So a Dinosaur on the edge of the farm is considered adjacent to a Dinosaur on the other side of the farm.