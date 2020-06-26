# CalculationOfTheNumberOfBottlesInACrate
Calculation of the number of bottles in a crate (Machine Vision) open CV
The algorithm used to implement Hough Circles is as follows:

Step 1: Read the image

Step 2: Gaussian Blur the image to reduce noise

Step 3: Edge detection using Canny Edge detector

Step4: For R from 10 to MAX(rows,cols)/2
For every pixel f(x,y)==255
For theta in range(0,360) with a step size of 10

x = x0 – R*cos (theta)
y = y0 – R*sine(theta)
Accumulator[R][x][y]+=1

Step 5: To normalize values perform, Accumulator=Accumulator/MAX(Accumulator)

Step 6: Construct circles for every R,x,y if the threshold is above a certain value. 
