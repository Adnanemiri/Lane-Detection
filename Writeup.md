
# Project : Finding Lane Lines

## Description

The pipeline takes an image as input and draws continuous lines over road lanes. First, we transformed the image from RGB to grayscale in order to decrease its size, and added Gaussian blur to suppress noise. Then, we applied the Canny algorithm to detect edges in the image and we’ve only selected edges inside a four sided polygon that delimits lanes. Next, we applied Hough transformation to detect line segments. In order to draw continuous lines, we extrapolated from highest segment to the lowest.

## Shortcomings

If the camera is not calibrated, the extrapolation form the highest segment to the lowest might draw a continuous line that does not fit the lanes.

## Improvements

We can use linear regression to draw continuous line segments.
