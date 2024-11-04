# SWE_CAP2_Game_Automation
# Programming the Farming Drone(Report)p0


# Introduction
"The Farmer Was Replaced" is the python base programming where the game we can control a farming drone, telling it to plant and harvest crops(carrot,pumpkin,sunflower,hay,tree,bush), add water and fertilizer and so more.
Our task is to develop a farm using the programming language to do activities like planting, watering, growing, harvesting different crops using and acquiring knowledge of using the loops and conditional statements making it entertaining.  

# Table of Contents
-[Code-Snippets-and-Explanation](#code-snippets-and-explanation)
-[Challenges and Learning](#Challenges-and-Learning)
-[References](#References)

## Step 1: Farming on 1 tile

**Code:**
```python
while True:
    if can_harvest():
    harvest()
else:
    do_a_flip()
    harvest()
```

**Explanation:**
The code runs an infinite number of times and harvest the grass if the condition is true but if it can't harvest right away, it flips before harvesting again.

**Demo:**
Video Demo:
![](IMG_2932.mp4)

**Notes**
- Using the code above I was able to get enough hay to unlock the tile.
- These features were unlocked too: plant, senses, expand, operators and variables.

# Challeges and Learning
 
## Challenges 
The challenge I faced was making mistake while typing harvest instead of harvest() because of not reading the instructions properly.

## Learnings
I learned how to harvest the hay using code and unlocked plant, senses, expand, operators and variables.

## References
1.[Resource 1](https://youtu.be/-hdhyKf2aN8?si=rxODvUsQhHm55cb-)
2.[Resource 2](https://youtu.be/gmJ357XAAdE?si=0bhCOu9eJkKWlv5y)


## Step 2: Farming on 3 tiles

**Code:**
```python
while True:
    if can_harvest():
        harvest()
        move(North)
```

```python
while True:
    if can_harvest():
        harvest()
    else:
        plant(Entities.Bush)
        do_a_filp()
        move(North)
        harvest()
    
```

**Explanation:**
First Code: Changed the code of hay so that instead of doing flip, the hay can harvest and move to north until I stop it.

Second Code: the code checks if the wood is ready,if so it harvest and if not the bush is being planted and to wait for it to grow it does the flip action and move north then again tries to harvest.

**Demo:**
Video Demo:
![](IMG_2946.mp4)

**Notes**
- Using the code above I was able to get enough hay and wood to unlock others.
- These features were unlocked too: carrots,debug,expaneded to 3*3.

# Challeges and Learning
 
## Challenges 
The challenges I faced was to code for the wood to harvest but with the help of youtube it was solved.

## Learnings
I learned how to harvest the hay faster, and within the while loop function, used if and else statement to check a condition to run the code for wood.

## References
1.[Resource 1](https://youtu.be/-hdhyKf2aN8?si=rxODvUsQhHm55cb-)
2.[Resource 2](https://youtu.be/gmJ357XAAdE?si=0bhCOu9eJkKWlv5y)

## Step 3: Farming on 3*3

**Code:**
```python
while True:
    plant(Entities.Bush)
    move(North)
    harvest()
    plant(Entities.Bush)
    move(East)
    harvest()
    plant(Entities.Bush)
    move(North)
    harvest()
    plant(Entities.Bush)
    move(West)
    harvest()
    plant(Entities.Bush)
    move(West)
    harvest()
    if can_harvest():
        harvest()
```

```python
while True:
    for x in range(get_world_size()):
        move(East)
        trade(Items.Carrot_Seed())
        for y in range(get_world_size()):
            if num_items(Items.Wood) < 1000:
                if can_harvest():
                    harvest()
            plant(Entities.Bush)
            move(South)    
```

```python
while True:
    for x in range(get_world_size()):
        move(East)
        trade(Items.Carrot_Seed())
        for y in range(get_world_size()):
            if num_items(Items.Carrot) < 1000:
                if can_harvest():
                    harvest() 
                 till()
                 plant(Entities.Carrots)
                 move(South) 
```

**Explanation:**
First Code: in the while loop, planted the bush, move it to north, harvests the wood, planted the bush, move it to east, harvests the wood, planted the bush, move it to north, harvests the wood, planted the bush, move it to west, harvests the wood,planted the bush, move it to north, harvests the wood and check if you can harvest again if yes, harvest.

Second Code: in the while loop,the code run repeatedly with no end. In the for statement of x it covers one dimension of the grid, in the for statement of y it covering the second dimension of the grid. If the number of wood items in your inventory is less than 1000, it performs a harvest() action. After checking for wood, it plants a bush at the current position using plant(Entities.Bush) and move to south and lastly, If there’s something ready to be harvested (can_harvest()), it harvests. If not, it moves south again.

Third Code: in the while loop, the code run repeatedly with no end, in for x loop it iterates across one dimension of the grid and For each position, it moves east and trades for carrot seeds with trade(Items.Carrot_Seed()). Inside the for y loop, this second loop iterates over the other dimension of the grid. Then If the number of carrots in your inventory is less than 1000, it harvest and till() function prepares the soil for planting, creating a spot for crops, plants a carrot in the tilled soil.After planting, it moves south to the next position in the grid.

**Demo:**
Video Demo:
![](IMG_2956.mp4)

**Notes**
- Using the code above I was able to get enough hay, wood, carrot to unlock others.
- These features were unlocked too: watering,pumpkin, multi_trade,utilities, lists, fertilizer,expaneded to 4*4.

# Challeges and Learning
 
## Challenges 
The challenges I faced were to code for the carrots to harvest and not being able to harvest on all the tails . 

## Learnings
I learned how to harvest useing nested loops to navigate a grid world and the while loop (for x in range(get_world_size())) represents moving horizontally, while the inner loop (for y in range(get_world_size())) represents moving vertically which helps to cover the entire area systematically. Learned to use the function till().

## References
1.[Resource 1](https://youtu.be/-hdhyKf2aN8?si=rxODvUsQhHm55cb-)
2.[Resource 2](https://youtu.be/gmJ357XAAdE?si=0bhCOu9eJkKWlv5y)

## Step 4: Farming on 4*4

**Code:**
```python
while True:
    for x in range(get_world_size()):
       for y in range(get_world_size()):
            if get_world_type() = Ground.Soil:
                till()
            if can_harvest():
                harvest()
            move(South)
        move(East)
harvest_grid()   
```

```python
while True:
    get_water()
    trade(Items.Empty_Tank)
    use_Items(Items.Water_Tank)
    move(North)
    get_water()
    trade(Items.Empty_Tank)
    use_Items(Items.Water_Tank)
    move(East)
    get_water()
    trade(Items.Empty_Tank)
    use_Items(Items.Water_Tank)
    move(North)
    get_water()
    trade(Items.Empty_Tank)
    use_Items(Items.Water_Tank)
    move(West)
    get_water()
    trade(Items.Empty_Tank)
    use_Items(Items.Water_Tank)
    move(West)
    if can_harvest():
        harvest()
```

```python
while True:
    for x in range(get_world_size()):
        move(East)
        trade(Items.Pumpkin_Seed())
        for y in range(get_world_size()):
            if num_items(Items.Wood) < 1000:
                if can_harvest():
                    harvest()
            plant(Entities.Pumpkin)
            move(South)    
```

```python
while True:
    for x in range(get_world_size()):
        move(East)
        trade(Items.Pumpkin_Seed())
        for y in range(get_world_size()):
            if num_items(Items.Pumpkin) < 1000:
                if can_harvest():
                    harvest() 
                 till()
                 plant(Entities.Pumpkin)
                 move(South) 
```

```python
while True:
    for x in range(get_world_size()):
       for y in range(get_world_size()):
            if % 2 == 0:
                if y % 2 == 0:
                    plant(Entities.Treee)
                move(South)
            elif x % 2 == 1:
                if y % 2 == 1:
                    plant(Entites.Tree)
                move(South)
        move(East)
plant_trees() 
```



**Explanation:**
First Code: Using the loop function representing x and y coordinates,if the ground type is Soil, it calls till() to prepare it for planting,if it can be harvested at the current position, it harvest then moves South after each y loop iteration and East after each x loop. The harvest_grid() at the end indicates to clean up any remaining resources.

Second Code:The loop continuously gathers water, trades empty tanks for full tanks, and uses these water tanks moving it in North, East, North, West, and West and if there's something to harvest, it harvests it.

Third Code: The loop goes through all the grid.For each x, the entity moves East and trades for pumpkin seeds and for each y, it harvests if there are less than 1000 wood items in inventory and plants a pumpkin at each cell and moves South.

Fourth Code: This is simlar to the but add till so the pumpkin can be planted and manages the pumpkin resources, only harvesting when less than 1000 pumpkins.

Fifth Code:  The loop goes through all the grid. The tree plants based on x and y coordinates.

**Demo:**
Video Demo:
![](IMG_2982.mp4)

**Notes**
- Using the code above I was able to get enough plant tree, pumpkin seed & pumpkin, water the plant, make farm to till(soil) to unlock others.
- These features were unlocked too: sunflower,polyculture, dictionaries and expaneded to 5*5.

# Challeges and Learning
 
## Challenges 
The challenges I faced were to code for the plant tree, pumpkin seed & pumpkin, water the plant,make farm to till,and grow the tree on all the till.

## Learnings
I learned to make the farm to till, and plant the seed of pumpkin and water it and grow it and harvest it with using loop functions, if,elif statement.rm6t 

## References
1.[Resource 1](https://youtu.be/-hdhyKf2aN8?si=rxODvUsQhHm55cb-)
2.[Resource 2](https://youtu.be/gmJ357XAAdE?si=0bhCOu9eJkKWlv5y)


## Step 5: Farming on 5*5

**Code:**
```python
while True:
    for x in range(get_world_size()):
        move(East)
        for y in range(get_world_size()):
            if num_items(Items.Power):
                if can_harvest():
                    harvest() 
                 till()
            plant(Entities.Sunflower)
            move(South)
  
```

**Explanation:**
This code is to plant sunflower's seed and harvest sunflower by using the loop function like in pumpkin and carrot.The if num_items(Items.Power) statement checks if the player has any "Power" items in their inventory. If they do, it harvest and it tills the soil, preparing the ground for planting and the code moves south by one step in the grid.

**Demo:**
Video Demo:
![](IMG_2989.mp4)


**Notes**
- Using the code above I was able to harvest sunflower so that it get power and speed up to unlock others.
- These features were unlocked too: treasure, maze, polyculture,dictionaries and other more.

# Challeges and Learning
 
## Challenges 
The challenges I faced were harvest sunflower in the farm with the question how to program and and the conditions where misplaced which leading to not functioning.

## Learnings
I learned the sequence of harvest → till → plant implies an automated farming cycle: clearing any mature crop, preparing the soil, and replanting.

## References
1.[Resource 1](https://youtu.be/-hdhyKf2aN8?si=rxODvUsQhHm55cb-)
2.[Resource 2](https://youtu.be/gmJ357XAAdE?si=0bhCOu9eJkKWlv5y)

# Google  drive Link
https://drive.google.com/drive/folders/1KphCFwFankuD-npzecqjNW0vR2FZKQHG?usp=sharing