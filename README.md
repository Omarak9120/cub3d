# ![Screen-Shot-2022-04-02-at-18 04 30](https://user-images.githubusercontent.com/28810331/161394297-4250216d-6d18-4fc9-9784-f95309fa3952.svg)
<div align="center">

<p align="center">

</p>

</div>

# Cub 3D
Project using raycasting, with minilibx.
Emulating FPS Wolfenstein game (1992)

https://user-images.githubusercontent.com/13866954/220087668-fa7b8233-d96a-4956-a566-6f538ef558c1.mp4

## Definitions / Infos:
* **Raycasting** is a rendering technique to create a 3D perspective in a 2D map.
* **Raycasting** is not the same as *raytracing*!
	- **Raycasting** is a fast semi-3D technique that works in realtime even on 4MHz graphical calculators.
	- while *raytracing* is a realistic rendering technique that supports reflections and shadows in true 3D scenes, and only recently computers became fast enough to do it in realtime for reasonably high resolutions and complex scenes.
* **DDA** - The **D**igital **D**ifference **A**nalyzer(DDA) algorithm is used to draw lines on a screen in an incrementally. The algorithm is called the Digital Difference Analyzer because it interpolates based on the difference between the start and end points. The algorithm itself is very easy to understand and implement.
* **Ray Casting**:
	1. Walls are always at 90° angle with the floor.
	2. Walls are made of cubes that have the same size.
	3. Floor is always flat.
* **FOV** - **F**ield **o**f **V**iew The player should be able to see what is in front of him/her. For this, we will need to define a field of view (FOV)
*  "To put the player inside the world, we need to define the player’s X coordinate, the player’s Y coordinate, and the angle that the player is facing to. These three attributes forms the 'point of view' of the player."
* **Fisheye Effect**: The fisheye effect is an effect you see if you use the real distance, where all the walls become rounded, and can make you sick if you rotate.

## Technical Details:
* DDA Will handle the "hit" in wall, looking the intersections of ray until hit the wall. __This framework will give to us what block was hited, not the distance__ If this was handled by looking for a fixed distance until the wall, we are not able to get a good design.
* DDA is able to identify block to  block where the ray will pass (x or y)
* 0.66 is a good size in FPS games (Size of plane)
* Formula: Dir + Plane + Multiplier (-1 a 1)

## Images:
Distance to wall:

![Distance to wall](https://permadi.com/tutorial/raycast/images/figure17.gif)

Calculating heading:

![Calculating heading](http://gamecodeschool.com/wp-content/uploads/2015/06/simple_game_graphics_movement_without_trigonometric_functions.png)

Pythagoras:

![pythagoras](https://upload.wikimedia.org/wikipedia/commons/3/39/Animated_gif_version_of_SVG_of_rearrangement_proof_of_Pythagorean_theorem.gif)


## More information:

* Libft allowed.
* GetNextLine allowed.
* Folder structure apply (managed by Makefile).
* No leaks are allowed.
* Norma must be run.

 ## To run:
```Bash
$ git clone --recursive https://github.com/omarak9120/cub3d.git
```

## Git sync main
```Bash
$ git clone
$ Make
$ valgrind --leak-check=full -q ./cub3d maps/rave.cub
$ and have fun with the game
```


## Links:
* [MinilibX](https://harm-smits.github.io/42docs/libs/minilibx)
* [Ray casting tutorial demos](https://github.com/permadi-com/ray-cast/tree/master/)
* [Ray Casting tutor](https://permadi.com/1996/05/ray-casting-tutorial-table-of-contents/)
* [Samples in js/HTML](https://github.com/permadi-com/ray-cast/tree/master/)
* [Demo](https://permadi.com/tutorial/raycast/demo/1/)
* [Trigonometry](https://en.wikipedia.org/wiki/Trigonometry)
* [Pythagoras](https://matematicabasica.net/teorema-de-pitagoras/)
* [Lodev - Raycasting](https://lodev.org/cgtutor/raycasting.html)
* [Manual do código](https://www.youtube.com/watch?v=J5K8qMCB-7o&list=PLLFRf_pkM7b6rBRoTOW64NKdltCLQNpW5)
