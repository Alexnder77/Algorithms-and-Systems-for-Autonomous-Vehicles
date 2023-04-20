# Algorithms-and-Systems-for-Autonomous-Vehicles
My solutions for the labs of Algorithms and Systems for Autonomous Vehicles (5EL272) at Umeå University


## Lab 1. Adversarial Attacks on Traffic Sign Recognition Model

Description: In this project, I explored the robustness of a deep learning model for traffic sign recognition against adversarial attacks. 
The model is based on the MobileNetV3 Large architecture, fine-tuned for the task of traffic sign recognition. 

The project is divided into two parts:
1. Training a traffic sign recognition model: Following a tutorial from DebuggerCafe, a MobileNetV3 model is fine-tuned on a traffic sign dataset using PyTorch.

2. Generating adversarial attacks and evaluating the model's robustness: The model is subjected to various adversarial attacks, including untargeted and targeted attacks, to assess its robustness.

The attacks used are as follows:

    Fast Gradient Sign Method (FGSM)
    Projected Gradient Descent (PGD) with untargeted and targeted variants

The accuracy of the attacked classifier is reported on the test set for each attack, and visualizations of successful attacks are displayed.

## Lab 2. PID Control
In this lab, the PIDControl Racetrack Twiddle.py program was modified to change the track shape to a circular racetrack with a radius of 50. 
The cross-track error (CTE) function was also adjusted accordingly. The twiddle() function was used to tune four different controller configurations: P, PI, PD, and PID. 
The final parameters for the PID controller provided a low tracking error.

In Task 2, the car's speed was increased to 10.0, which could cause the car to lose control. 
To maintain control, the timestep size (dt) was adjusted by increasing the sampling rate. 
The PID controller was tuned with twiddle() for this higher speed, and different timestep sizes were tried to achieve a low tracking error. 
Reducing dt to 1/10 led to a better error result, but a good error was already achieved with dt = 1. The PID gains for dt = 1/10 were obtained, and the diagram of the last N steps was presented.

## Lab 3. Simulating highway driving
In Lab 3, the goal is to modify the highway-env repository, specifically the highway_env.py file, to introduce a penalty for changing lanes during highway driving. This is done to encourage the agent to maintain its current lane when possible. The lab involves the following steps:

1. Fork the highway-env repository and modify the highway_env.py file to include a penalty term for lane changes.
2. Replace the original pip installation command with the path to the forked repository.
3. Train the agent with various values of lane_change_reward and different environments with varying complexity.
4. Test the agent in environments with different configurations and observe its behavior.
5. Document and submit the results, including recorded videos during testing, screenshots, and descriptions of observations for each configuration, with a focus on configurations that only differ in lane_change_reward.
