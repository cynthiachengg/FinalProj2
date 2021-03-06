# Raytastic

## What?
  This is a Raycastor made with Processing. It projects rays across a 2D map, which then come to represent vertical stripes
  on the screen. Basically, a limited 3D projection. No spheres, no prisms. But it's cool and doesn't lag.

## Who?
  Cynthia Cheng and Max Zlotskiy.

## How?
  Vectors, image manipulation, and an unecessary amount of levels of abstraction (as is typical of Java programs).
  
## Can has try?
  1. clone the Repo
  2. open Processing
  3. point it to the `.pde` files in `Main/`
  4. run it
  5. Use *left* and *right* arrow keys to move your head(camera)
  6. Use *up* key to move forward and *down* key to move backwards
  7. Press the spacebar to open/close/toggle the door. The door looks like a bookshelf.
  8. You may enter the room through the door, or roam into the infinite brown expanse

## Bugs
  You can pass through walls. If the `world1.txt` file has improper formatting, or if any of the images are missing,
  the program will crash. There must be padding in the world file. Placing Solids at x=0 or y=0 produces mind-blowing
  visual glitches.

## Plans
  We plan to implement a functional collision detection system. We also plan to add a main menu screen to provide
  keyboard instructions. The main menu screen should also lead to a map editor and/or a world selection screen.
  As of now, the only way to customize the World is to edit the textfile. <u>DO NOT EDIT IT UNLESS YOU KNOW WHAT
  UR DOING BRO.</u> Every line must be the same length, even if it has spaces, and no `\r` may be present.
  
  We plan to add a menu or keyboard shortcut to change render distance (currently 10) and resolution. Render distance
  affects how far the RayCastor will check for objects. The resolution affects how many rays the Camera projects,
  and therefor how smooth the rendering looks.

## Devlog

- May 29, 2017: 
  created repo in class, decided on final project topic (approved) - ray castor  
  wrote basic ray class with instance variables, constructor, toString (started using Pvector- Processing class)

- June 1st, 2017:
  Wrote camera class which interacts with Ray to create the projection of images. 
  Methods to create an "interative" ray and created mathods to "rotate" the camera.
  The camera also has a customizable resolution now.
  
- June 4th, 2017:
  The terrain is now stored inside of a World class. The World stores Solids by their coordinates, with
  a very fast cordinate lookup system. This also induced a refactoring of the Raycasting and Texture classes.
  Textures no longer draw themselves to the screen, but rather return an image buffer for Renderer to use.

- June 7th, 2017:
  Got Image Textures to work. Got HD textures to work too.

- June 9th, 2017:
  The background has a sky and ground, replacing the black void. Added some rudimentary movement.
  
- June 10th, 2017:
  Added doors and beacons.

- June 11th, 2017:
  Fixed all the bugs inolved with movement. Also added the ability to load a World from a file.
