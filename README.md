# bad-apple
 Bad Apple printed out on the console with Python!

You can either `git clone` or download a ZIP of this repository. 

`git clone https://github.com/DinhPhongNe/TouHou-BadApple.git`

Then, ensure that you set your terminal to the directory of this repository. 

`cd bad-apple`

Install the necessary dependencies and packages by using:

`pip install -r requirements.txt`

And to run the code:

`python touhou_bad_apple_v4.0.py`

And just follow the on-screen prompts. 

# Performance optimizations
Currently, my implementation of a rudimentary static `time.sleep()` function results in an incremental error over time. 
This thus leads to the frame accuracy drifting. 
 
# Functions
The main functions will be listed here. 

## play_video()
Reads the files from the previously generated ASCII .txt files and prints it out onto the console. 

## play_audio()
Plays the bad apple audio track. 

## progress_bar(current, total, barLength=25)
A simple progress bar function that generates the status of both frame extraction and ASCII frame generation. 
This code was taken from a [StackOverflow thread](https://stackoverflow.com/questions/6169217/replace-console-output-in-python).

`current` is the current value/progress of the process. 

`total` is the desired/intended end value of the process.

`barLength=25` sets the length of the progress bar. (Default is 25 characters)

## ASCII Frame generation
Not a particular function, but a group of functions.

```
resize_image()

greyscale()

pixels_to_ascii()
```
These functions are called in the `ascii_generator()` function to convert image files to ASCII format and stores them into .txt files. 

Note that the ASCII conversion code is not original, and was taken from 
[here](https://github.com/kiteco/python-youtube-code/blob/master/ascii/ascii_convert.py).