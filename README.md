# javascript-enemy-movements

Set up canvas similar to previous spriteAnimation and parallax projects
Create temporary enemy1 object variable with xy coordinate of 0 and width height of 200
Create an animate function and use the fillRect() method on ctx with enemy1's property values
Add requestAnimationFrame(animate) to animate and clearRect method on ctx at the start of the animate function to clear canvas everytime it animates on a new frame
Call animate() after the animate function to animate
Create a class Enemy and input the temporary enemy1's properties inside the constructor with this keyword
Comment out the temp enemy1 variable and initialize a new constant enemy1 variable, assigning it to the new Enemy() class you just created
To add more enemies you would initialize new variables for each of them but you would need to hardcode the speed which is not efficient
You would need to create a shared class method in the constructor named update() and put all the enemy variables speed calculation inside
Create the update() function below constructor and use the increment operator on xy coordinates with this keyword
You can now remove all increment operators in the animate function and access the update method inside the Enemy the class with enemy1.update()
Create a draw function after update to draw all enemies at the same time instead of using fillRect method inside animate
Move ctx.fillRect from animate to draw and fill the parameters using the this keyword instead
To access this method in animate, do the same thing as you did with update with enemy1 and remove ctx.fillRect from animate
Currently, the values inside the constructor properties are fixed so all enemies spawn and move at the same area and direction
To randomise them, employ the Math.random method for xy values between 0 and the width for x and height for y (Math.random() multiplied by width/height)
You can only create 1 enemy using enemy1 variable
Comment out enemy1 and create a global variable numberOfEnemies with a value of 100 and create a for loop using the hardcoded value as baseline for now
Create a new global variable called enemiesArray and assign it an empty array
Push an instance of new Enemy() to the above array everytime the for loop runs till it reaches its quota according to numberOfEnemies
Since enemy1 does not exist anymore, remove the remnants inside animate
To access the newly created enemiesArray that you have just for looped, use the forEach method inside animate and for each enemy call the update and draw method on it
Now you should see the boxes moving at the same speed in the same direction from different randomised locations
Create a new property inside the constructor called speed and randomise it between -2 and +2 (left and right) using Math.random() \* 4 - 2
Now instead of using the default increment operator in update, increment it by this randomised speed instead
Now initialize global variable enemyImage assigning it to new Image() method
Link it to the source enemy1.png
Call it with drawImage method on context inside draw method, using enemyImage and xy coordinates as parameters
Add width and height to drawImage as additional parameters
Create new properties called spriteWidth and spriteHeight inside the constructor with the values taken from the png you want to use
Since we can use up to 9 parameters in drawImage, you can crop out the image you are using inside the strokeRect method to only 1 by specifying with additional parameters(refer to spriteAnimation js for this) for sx sy sw and sh
Using hardcoded values for width and height will squeeze the much larger width and height of the sprites insde the boxes
Move the width and height of the constructor below sprite width and height and assign them to the width and height of the sprite to get the original size back
Divide assigned values of the width and height by lets say 3 to get a smaller aspect ratio
//TBC
