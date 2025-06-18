# 🧭 Problem 2: Cube Conundrum *(Minecraft Edition)*

<video width="640" height="360" controls autoplay loop muted>
  <source src="img/problem2.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

You’ve been summoned to the **Skyblock Island**, a floating ruin where an Elf offers a puzzling game involving enchanted **Minecraft cubes**. These cubes—**redstone**, **lapis**, and **emerald**—are hidden in a magical bag. Each round, the Elf draws cubes, shows them to you, and returns them to the bag.

Each session is logged as a “Game,” with line entries like:

```
Game 1: 3 blue, 4 red; 1 red, 2 green, 6 blue; 2 green
```

Here, “blue” corresponds to **lapis**, “red” to **redstone**, and “green” to **emerald**. Each draw is temporary—cubes go back in the bag after being shown.

---

## 🧱 Part 1

The Elf wants to know which games *could* have happened if the bag started with exactly:

- **12 redstone**
- **13 emerald**
- **14 lapis**

A game is *possible* if **every draw in that game** never shows more cubes of any color than are in the bag.

### 🎯 Your Task:
- Identify all possible games under the 12/13/14 limit.
- **Sum the IDs** of those games.

### 🧪 Example:

```
Game 1: 3 blue, 4 red; 1 red, 2 green, 6 blue; 2 green
Game 2: 1 blue, 2 green; 3 green, 4 blue, 1 red; 1 green, 1 blue
Game 3: 8 green, 6 blue, 20 red; 5 blue, 4 red, 13 green; 5 green, 1 red
Game 4: 1 green, 3 red, 6 blue; 3 green, 6 red; 3 green, 15 blue, 14 red
Game 5: 6 red, 1 blue, 3 green; 2 blue, 1 red, 2 green
```

- Games **1**, **2**, and **5** are possible with the cube limits → sum = **8**.

In the example above, games 1, 2, and 5 would have been possible if the bag had been loaded with that configuration. However, game 3 would have been impossible because at one point the Elf showed you 20 red cubes at once; similarly, game 4 would also have been impossible because the Elf showed you 15 blue cubes at once. If you add up the IDs of the games that would have been possible, you get 8.


Determine which games would have been possible if the bag had been loaded with only 12 red cubes, 13 green cubes, and 14 blue cubes. What is the sum of the IDs of those games?

---

## ⚙️ Part 2

The Elf introduces a new scoring rule: for each game, consider each color **independently**, and use the **maximum number of cubes drawn** of that color across all draws in the game.

Calculate the **“power rating”** of the game as:

```
(max redstone drawn) × (max emerald drawn) × (max lapis drawn)
```

Sum these power ratings for **all games** in your input.

### 🧪 Example (continued):

- Game 1 max: 4 redstone, 2 emerald, 6 lapis → 4 × 2 × 6 = 48
- Game 2 max: 1 redstone, 3 emerald, 4 lapis → 1 × 3 × 4 = 12
- Game 3 max: 20 redstone, 13 emerald, 6 lapis → 20 × 13 × 6 = 1560
- Game 4 max: 14 redstone, 3 emerald, 15 lapis → 14 × 3 × 15 = 630
- Game 5 max: 6 redstone, 3 emerald, 2 lapis → 6 × 3 × 2 = 36

**Sum = 48 + 12 + 1560 + 630 + 36 = 2286**

---

## 📝 Your Input

Replace with your puzzle input. Then:

- **Part 1 answer** = sum of valid game IDs under the 12/13/14 limit  
- **Part 2 answer** = sum of power ratings across all games

Happy blocky scoring, and may your redstone, emerald, and lapis cubes be ever in your favor!


