# RL_Aircraft
Training Aircrafts to fly in terrains with mountains and rocks as obstacles and goal to pass through checkpoints that are located approximately after every 100 m.

RL_Aircraft is our project for Course CS662- Mobile Virtual Reality and Artificial Intelligence

# Requirements:- 
1.) You should have Unity Hub, Unity Editor and Anaconda installed on your machine.

# To play the game
1.) Clone the Repository using git clone https://github.com/SouravSehgal-3009/RL_Aircraft on your pc/laptop.
2.) Open the project on Unity Editor and navigate to Assets/Aircraft/Scenes
3.) Open the scene **Desert** and start playing.
4.) There is an **Airplane Player** (red colour) which will be controlled by the user while four other planes will be flying according to the network trained. There are two networks trained: one using **PPO(Proximal Policy Optimization)** and other using **Imitation Learning**.
5.) The goal is to pass through the checkpoints and compete with the aircrafts that have been trained using the reinforcement learning. Don't worry atleast you can perform better than us :) if network used is trained using Imitation Learning.

# Do you want to train your own neural network using PPO
1.) Open Anaconda Prompt on your laptop.
2.) Now, first of all create a virtual environment in the project folder.
    ```bash
    conda create -n myproj python=3.7.7
    ```
    We are using Python Version 3.7.7 for our project.
3.) Now activate the virtual environment using:
    ```bash
    conda activate myproj
    ```
4.) Install ml-agents using
    ```bash
    pip install ml-agents==0.16.0
    ```
5.) Now run the command:
    ```bash
    mlagents-learn config/trainer_config.yaml --curriculum config/curricula/AircraftLearning.yaml --run-id=aircraft_01
    ```
    (You can see the configuration file and the curriculum file in config folder and change them as per your convenience)
    Now navigate to Assets/Aircraft/Scenes and open Training Scene and click the Play Button.
6.) The progress after every 32000 steps will be displayed on the shell and you can hit Ctrl+C if you are satisfied with the model trained so far.
7.) The trained model will be saved in Models folder of the project.
8.) You can add the trained model in **AirplaneLearning** Prefab under **Model** in **Behaviour Parameters** Section in Inspector Window of AirplaneLearning and can play the game in Desert Scene and compete with your own built network.

# Do you want to train your own neural network using Imitation Learning
1.) Open Anaconda Prompt on your laptop.
2.) Now, first of all create a virtual environment in the project folder.
    ```bash
    conda create -n myproj python=3.7.7
    ```
    We are using Python Version 3.7.7 for our project.
3.) Now activate the virtual environment using:
    ```bash
    conda activate myproj
    ```
4.) Install ml-agents using
    ```bash
    pip install ml-agents==0.16.0
    ```
5.) Now run the command:
    ```bash
    mlagents-learn config/imitation_config.yaml --curriculum config/curricula/AircraftLearning.yaml --run-id=aircraft_01
    ```
    (You can see the configuration file and the curriculum file in config folder and change them as per your convenience)
    Now navigate to Assets/Aircraft/Scenes and open Imitation Scene and click the Play Button
6.) The progress after every 32000 steps will be displayed on the shell and you can hit Ctrl+C if you are satisfied with the model trained so far.
7.) The trained model will be saved in Models folder of the project.
8.) You can add the trained model in **AirplaneLearning** Prefab under **Model** in **Behaviour Parameters** Section in Inspector Window of AirplaneLearning and can play the game in Desert Scene and compete with your own built network.

**Future Scope**
We are thinking of adding Virtual Reality in the game in the future.

Made by:
[Sourav Sehgal](https://github.com/SouravSehgal-3009)
[Rohan Raj Kansal](https://github.com/BeingHomosapien)




