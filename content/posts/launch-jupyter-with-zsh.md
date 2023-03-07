+++
title="Launching A Jupyter Notebook using a ZSH/Bash script"
date="2023-03-04T18:06:01.000Z"

[taxonomies] 
tags = ["rants", "tutorial"]
+++

### The ZSH script

```shell
#!/bin/zsh

cd Desktop/mphil/prog
source a1renv/bin/activate
python3 -m ipython kernel install --name=a1renv
jupyter notebook
```
^ That there is the script

### Why?

I wanted seperate environments for my different notebooks so that they did not fight with my existing installations.

### Explanation of the script

The directory is change to somewhere I want. The environment is activated. The python kernel is told that I have an environment, but I guess that is verbose and not needed. And then the Jupyter notebook is launched.

### Rant!

The rant tag is there for a reason. Python package management is near bollocks. It's at least better than C (I worked with Arduino and it felt like pain) but using a bit of Rust, Cargo is a God-Send. I just don't get how hard it would be to rejig the package manager. Virtual Environments that conflict with something else globally. Like why is there a global package area and a local virtual environment and if they want to talk to each other why do I need to edit a random text file I have no idea about taking help from a random Medium article and it somehow all works. But anyways. Python is supposed to be an "easy" language and is very good for prototyping things on the fly. I just hoped there were better libraries for Rust or something else so that after protyping.