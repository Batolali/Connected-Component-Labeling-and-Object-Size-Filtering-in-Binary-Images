# Connected-Component-Labeling-and-Object-Size-Filtering-in-Binary-Images


This Python program performs connected component labeling on a binary image. First, it reads a grayscale image named cc_input.png and converts it into a binary image. In this binary image, all pixels with intensity values below 128 are set to white (255), and all others are set to black (0).

Next, the program labels each connected component in the image using a simple algorithm that examines the pixel's neighbors to the left and above. If both neighbors are background pixels (value 0), a new label is assigned. If one or both neighbors already have a label, the current pixel inherits the appropriate label. In cases where the neighboring labels differ, the algorithm assigns the smaller label and updates the previous occurrences of the larger label to ensure consistency.

Once all components are labeled, the labels are normalized so they follow a sequential order, starting from 0. The program then calculates the height and width of each component by finding the minimum and maximum coordinates occupied by each label.

After computing the size of all components, the program calculates the average height and width. It then identifies and highlights only those components that are larger than average by drawing a rectangle around them using the matplotlib.patches.Rectangle function.

Finally, the output image with rectangles drawn around the selected components is saved as compinent_image.png and displayed on the screen.
