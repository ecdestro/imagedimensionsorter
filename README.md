# imagedimensionsorter
A shell script for sorting folders of images into landscape or portrait folders

This script depends on imagemagick's "identify" utility to extract the dimensions of the image, which it then divides the width by the height to get a ratio using awk. Awk compares the resulting ratio to either above or below 1. Anything between 0 and 1 is portrait, anything greater than 1 is landscape.

This can be refined further to make classifications of sorts, such as if the ratio equals some number like 1.7777777778 then the image can scale to any 16 by 9 resolution screen. A ratio of 1.6 will fit most Mac screens that run on 16 by 10 resolutions.
