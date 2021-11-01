# Use_PlaNet_to_solve_customirized_reaching_task_by_pixel_observation

Reinforcement learning(RL) has been widely used in the robotics area to solve a series of object manipulation tasks and achieve satisfactory results. For example, the reaching, 
pushing,sliding, picking and placing tasks in the OpenAI gym environment has been solved accurately by a few reinforcement learning algorithms. However, it is a challenge 
to replicate the current results from simulators to real robotics systems. This is because, in the real robotics system, it is hard to evaluate the real-time state, such as the
 position and pose of the robot and target object, but this can be done easily in the programmed simulator. Image-based observation can be used to solve the above problem, because
 the cost of extracting images is far lower. It has made decent progress in some other tasks.\
 
 In this experiment, the image is directly and completely used as input to train the agent, without relying on any environmental data and robot data. The structure of Google PlaNet has been adjusted to make it compatible with our development environment.
 
 ## Intallation
* Clone or download this repository to your local PC.
* The environment used in this experiment is in another folder of mine, please see:
https://github.com/wq13552463699/UR5E_robot_gym_env_Real_and_Sim/tree/main/Simulation
Please clone the content in this link, and put all the files together within this repository in you local PC
* pip install -r requirements.txt 

## Result
After about 500 epochs of training, the robotic arm can reach the target accurately. Please see the following video\
https://www.youtube.com/watch?v=7SAwoP7Y8qY
The 2 images in the left hand side are all the observations for the agent.

### Lose cureves
<img src="https://github.com/wq13552463699/Use_PlaNet_to_solve_reaching_task_by_pixel_observation/blob/main/pictures/2.png" width="800" >\
