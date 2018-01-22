# Flappy Bird Clone Instructions
## Step 0 - Preparation
Go into the media lab with your partner and have Mr. Dockett take a side view photo of their head facing to the right. Once everyone's photo has been taken, Mr. Dockett will upload all of the photos to the tacher share for you to get. 

## Step 1 - Download & Open the Starter Code
Download this repo as a zip folder. Once complete, extract the files to your desktop. Open the parent folder and double click "c game.sln."
This will open Visual Studio.

## Step 2 - Photoshop
Use Adobe Photoshop to open the photo and the magnetic lasso (l) tool to trace around their head. Right click on the image and click "Select inverse." Double click the layer in to turn it into a regular layer instead of a background layer (removing the lock). Selct the eraser tool (e) and erase the space around the student's head. Crop the photo to a square with the player's head centered. Save or export the photo as a png file with transparency. It is important to make sure that your image has transparency. An image without transparency will just have a white background.

## Step 3 - Change the Bird to a Head.
In the form designer, select the bird, then right click on it and select "choose image...." Select the "Local Resource" radio button then click the upper "Import..." button. Find the player's head image and click "Open." The bird image has now been replaced by the player's head.

## Step 4 - Change the Gravity setting.
Open the code editor for form1.cs and go to line 111. Change the number assigned to acc[1] to change gravity. Almost no gravity is "0.01" Tons of gravity is "10." Default gravity is "0.45."

## Step 5 - Change the Vertical Space Between Pipes.
In form1.cs on line 29, change the value for gap to change the vertical space between pipes. The space is measured in pixels. A bigger number means more space and in turn makes the game easier. Setting this value to "0" would make the game impossible.

## Step 6 (If there is time) - Jump with "Space"
In form1.cs, change line 140 from:

if (e.KeyCode == Keys.Up) { vel[1] = -10; fly.Play(); } // JUMP!

to:

if ((e.KeyCode == Keys.Up) || (e.KeyCode == Keys.Space)) { vel[1] = -10; fly.Play(); } // JUMP!
