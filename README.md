# Seeded-Propagation
pure python generative art

Output Art examples can be found here:
https://github.com/ovjanman/Seeded-Propagation/issues/3
![ezgif-2-19e847c877](https://user-images.githubusercontent.com/68125226/170067026-d73a39f5-df11-4ddc-bc37-262a971ad372.gif)


This project is used to create generative "propagative" art using python. 

Licensing:
Please feel free to adapt and use this project as you see fit, with credit cited back to this repo. PRs are welcome.

Requirements:
A jupyter notebook/jupyterlab enviornment with PIL installed. 

How to use:
More detailed instructions can be found within the notebook file

Video outputs:
The program outputs a series of PNGs to the output folder. These can be turned into an mp4 using something like blender. A static B&W image of the propagation map is also outputted at the end of the script

Behaviour discussion:
when one agent (snake) encounters an obstacle it has the chance of going back (on itself) and left or back and right. In theory them going parralel to the obstacle would be also an option, however due to the basic way I do the collision detection (just an array representing the pixel grid that gets filled up as the agents travel over pixels) it would mean you'd get two colours directly next to eachother which I don't think looks all that great. Some better code to have the agents turn to go parralel a few pixels away from the obstacle would be ideal.

There's also a slight (about 1 in 500 per agent update) chance of an agent just randomly picking a new direction, simply to add some extra randomness to ones which otherwise would go straight and hit the wall.

My collision is far from perfect, with diagonal perpendicular collisions not being registered leading to agents jumping over diagonal lines. However in the end I actually don't mind this effect as it prevents agents from getting stuck in corners very early on.


