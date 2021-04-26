[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/43851024-320ba930-9aff-11e8-8493-ee547c6af349.gif "Trained Agent"
[image2]: https://user-images.githubusercontent.com/10624937/43851646-d899bf20-9b00-11e8-858c-29b5c2c94ccc.png "Crawler"


# Project 2: Continuous Control

### Overview

In this project, we implement the Deep Deterministic Policy Gradient reinforcement learning technique of Lillicrap et al (2015) to guide the motions of a double-jointed robotic arm in an adaptation of OpenAI Gym's Reacher Environment to the targeted destinations. The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular momentum of the arm. The actions are represented by 3 number corresponding to torque in the two joints between 1 and -1. The task is episodic in nature. A reward of +0.1 is provided for each step that the agent's hand is in the target position, so our goal is to keep the agent's hand in the target location as much as possible. We consider the environment to be solved when the agent is able to achieve a score of +30 over 100 consecutive episodes. 
![Trained Agent][image1]


### Instructions - Dependencies
1. Create (and activate) a new environment with Python 3.6.

    Linux or Mac:
    ```
    conda create --name drlnd python=3.6
    source activate drlnd
    ```
    Windows:
    ```
    conda create --name drlnd python=3.6 
    activate drlnd
    ```
2. Follow the instructions in [this repository](https://github.com/openai/gym) to perform a minimal install of OpenAI gym.

    - Next, install the classic control environment group by following the instructions here.
    - Then, install the box2d environment group by following the instructions here.

3. Clone the repository, and navigate to the python/ folder. Then, install several dependencies.
    ```
    git clone https://github.com/udacity/deep-reinforcement-learning.git
    cd deep-reinforcement-learning/python
    pip install .
    ```

4. Create an IPython kernel for the drlnd environment.
    ```
    python -m ipykernel install --user --name drlnd --display-name "drlnd"
    ```

5. Before running code in a notebook, change the kernel to match the drlnd environment by using the drop-down Kernel menu.


### Instructions - Project Code
1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:

    - **_Version 1: One (1) Agent_**
        - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
        - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
        - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
        - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)

    
2. Place the file in the DRLND GitHub repository, in the `p2_continuous-control/` folder, and unzip (or decompress) the file. 

### Instructions - Executing the code

Run all cells in `Continuous_Control.ipynb`

### The files

- **Continuous_Control.ipynb**: Contains the code to run the agent in the environment
- **dqn_agent.py**: Code for the agent
- **dqn_model.py**: Code defining the deep Q Network 
- **checkpoint.pth**: Pytorch model weights