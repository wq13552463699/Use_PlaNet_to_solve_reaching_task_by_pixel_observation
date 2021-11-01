# Use_PlaNet_to_solve_customirized_reaching_task_by_image_observation

Reinforcement learning(RL) has been widely used in the robotics area to solve a series of object manipulation tasks and achieve satisfactory results. For example, the reaching, 
pushing,sliding, picking and placing tasks in the OpenAI gym environment has been solved accurately by a few reinforcement learning algorithms. However, it is a challenge 
to replicate the current results from simulators to real robotics systems. This is because, in the real robotics system, it is hard to evaluate the real-time state, such as the
 position and pose of the robot and target object, but this can be done easily in the programmed simulator. Image-based observation can be used to solve the above problem, because
 the cost of extracting images is far lower. It has made decent progress in some other tasks.
 
 In this experiment, the image is directly and completely used as input to train the agent, without relying on any environmental data and robot data. The structure of Google PlaNet has been adjusted to make it compatible with our development environment.
 
 ## Intallation
* Clone or download this repository to your local PC.
* The environment used in this experiment is in another folder of mine, please see:
https://github.com/wq13552463699/UR5E_robot_gym_env_Real_and_Sim/tree/main/Simulation
Please clone the content in this link, and put all the files together within this repository in you local PC
* pip install -r requirements.txt 

## Result
**!!!After about 500 epochs of training, the robotic arm can reach the target accurately. Please see the following video\
https://www.youtube.com/watch?v=7SAwoP7Y8qY \
The 2 images in the left hand side are all the observations for the agent.**

### Lose cureves
<img src="https://github.com/wq13552463699/Use_PlaNet_to_solve_reaching_task_by_pixel_observation/blob/main/pictures/2.png" width="1000" >\
Since I use a customized reward function (goal-based reward function), the score is not fixed. You can assume that every epoch with around 300 is successful. So at the beginning, the agents rarely reach the target, and after 400 epchos of training, it rarely failed with the success rate above 95%

<img src="https://github.com/wq13552463699/Use_PlaNet_to_solve_reaching_task_by_pixel_observation/blob/main/pictures/1.png" width="1000" >\
<img src="https://github.com/wq13552463699/Use_PlaNet_to_solve_reaching_task_by_pixel_observation/blob/main/pictures/3.png" width="1000" >\
<img src="https://github.com/wq13552463699/Use_PlaNet_to_solve_reaching_task_by_pixel_observation/blob/main/pictures/4.png" width="1000" >

## Further Concern
Using images directly as input has the following disadvantages:
* The dimensionality is high and the convergence speed is slow.
* There is a lot of redundant information and noise in the image data, which can be misleading.
* There is a lot of potential information in the image to be discovered.\
We need to develop a complete representation model to overcome the above problems. See my other folder for details：\
https://github.com/wq13552463699/One_to_Multi_Representation

## Reference
https://github.com/Kaixhin/PlaNet \
https://github.com/openai/gym \
https://github.com/openai/mujoco-py

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change\
Please make sure to update tests as appropriate.
