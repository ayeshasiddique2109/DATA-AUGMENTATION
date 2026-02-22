# DATA-AUGMENTATION
The script utilizes the ImageDataGenerator class to apply the following transformations:
Rotation up to 40 degrees.
Shearing/Slanting the image by 20%.
Randomly zooming in or out by 20%.
Flipping/Horizontal mirroring.
Adjusting intensity between 50% and 150%.
Fill Mode Uses 'nearest' to fill in empty pixels created by transformations.
# Preprocessing Pipeline
The script follows a standard preprocessing pipeline:
Loading converts the image into a 3D NumPy array.
Reshaping adds a "batch" dimension to make the array 4D, as required by Keras:x_{shape} = (1, height, width, channels).
Flowing the datagen.flow() method creates a loop that generates and saves images to the disk automatically until the counter reaches 40.
