MLRocket - Unity Rocket Navigation with ML-Agents
This project simulates a rocket navigating through space using machine learning to autonomously avoid obstacles. The rocket is trained to navigate to a target endpoint while dodging various obstacles like asteroids and dust clouds. The simulation leverages Unity's ML-Agents toolkit with reinforcement learning for training the rocket's autonomous navigation.

Features
Simulated space environment with dynamically created obstacles.
Autonomous rocket navigation using reinforcement learning.
Configurable reward and training settings for custom training sessions.
Real-time monitoring with TensorBoard.
Prerequisites
To run this project, you will need:

Unity 2020.3.18f1 or newer.
Unity ML-Agents Toolkit (version 0.28.0 or later).
Python 3.8+ with the following packages:
mlagents
numpy
tensorflow or pytorch (optional, depending on preference)
Installation
Clone this repository
Clone the repository to your local machine:

bash
Skopiuj kod
git clone https://github.com/tslapczynski/MLRocket.git
cd MLRocket
Install Unity ML-Agents Toolkit
Follow the ML-Agents installation instructions to set up ML-Agents in your Unity project. Typically, this involves running:

bash
Skopiuj kod
pip install mlagents
Open the Project in Unity

Open Unity Hub, and click on Add.
Select the MLRocket project folder.
Open the project in Unity 2020.3.18f1 or a compatible version.
Configure the Environment

Open the scene MLRocketScene located in the Assets/Scenes/ folder.
Ensure ML-Agents is configured properly by checking the Agent component on the rocket object.
Modify training parameters in rocket_navigation_config.yaml if needed.
Start Training the Rocket

Open a terminal or command prompt in the project directory.
Run the training process with:
bash
Skopiuj kod
mlagents-learn config/rocket_navigation_config.yaml --run-id=rocket_navigation
Press the Play button in Unity to begin training. The rocket should start learning to navigate the environment.
Monitor Training with TensorBoard (optional)

To monitor the training progress, run:
bash
Skopiuj kod
tensorboard --logdir=results
Open http://localhost:6006 in your browser to view training metrics.
Project Structure
Assets/ - Unity assets, including the rocket model, obstacles, and scenes.
config/rocket_navigation_config.yaml - ML-Agents configuration file for training parameters.
results/ - Directory where training results are saved.
scripts/ - Contains Python scripts for data processing and model evaluation.
Troubleshooting
Unity Compatibility – Ensure you’re using Unity 2020.3.18f1 or newer for best results with ML-Agents.
ML-Agents Version – This project is compatible with ML-Agents 0.28.0 or newer. Check compatibility if you encounter issues.
Training Performance – For faster training, consider using a machine with a powerful GPU.
License
This project is licensed under the MIT License. See the LICENSE file for more information.
