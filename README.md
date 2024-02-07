# udacity-navigation
## Project environment details
This repository solves the first project assignment of Udacity's Deep Reinforcement Learning Nanodegree. 

Included is a self-learning agent that learns to navigate in a virtual world based on the Unity engine to collect yellow bananas while avoiding blue bananas. Every yellow banana collected rewards one point to the agent while every blue banana costs one point.

![banana](images/banana.gif)

The environment's state gives the agent a 6x6 pixel view on its surroundings. Additionally, one input is dedicated to the agent's velocity, adding up to 37 state parameters. 

Based on this perception the agent may choose one of four actions, e.g. turn left or right and move forward or backward.

The challenge is considered solved if the agent manages to collect more than 13 points in average over 100 consecutive episodes.

## Getting Started

Clone this github repository.

Download the Unity environment from one of these links:

* [Linux](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
* [Mac OSX](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
* [Windows (32-bit)](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
* [Windows (64-bit)](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)

Then, place the file in the folder of the GitHub repository and make sure the dependencies listed below have been fulfilled.

In order to train the agent, use Navigation.ipynb and adjust the link to the Unity environment according to your setup.

## Dependencies
(copied from https://github.com/udacity/Value-based-methods/blob/main/README.md)

To set up your python environment to run the code in this repository, follow the instructions below.

1. Create (and activate) a new environment with Python 3.6.

	- __Linux__ or __Mac__: 
	```bash
	conda create --name drlnd python=3.6
	source activate drlnd
	```
	- __Windows__: 
	```bash
	conda create --name drlnd python=3.6 
	activate drlnd
	```
	
2. Follow the instructions in [this repository](https://github.com/openai/gym) to perform a minimal install of OpenAI gym.  
	- Install the **box2d** environment group by following the instructions [here](https://github.com/openai/gym#box2d).
	
3. Clone the repository (if you haven't already!), and navigate to the `python/` folder.  Then, install several dependencies.
```bash
git clone https://github.com/udacity/Value-based-methods.git
cd Value-based-methods/python
pip install .
```

4. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `drlnd` environment.  
```bash
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```

5. Before running code in a notebook, change the kernel to match the `drlnd` environment by using the drop-down `Kernel` menu. 
