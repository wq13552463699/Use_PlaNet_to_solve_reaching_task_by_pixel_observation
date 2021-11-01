Reinforcement learning(RL) has been widely used in the robotics area to solve a series of object manipulation tasks and achieve satisfactory results. For example, the reaching, 
pushing,sliding, picking and placing tasks in the OpenAI gym environment has been solved accurately by a few reinforcement learning algorithms. However, it is a challenge 
to replicate the current results from simulators to real robotics systems. This is because, in the real robotics system, it is hard to evaluate the real-time state, such as the
 position and pose of the robot and target object, but this can be done easily in the programmed simulator. Image-based observation can be used to solve the above problem, because
 the cost of extracting images is far lower. It has made decent progress in some other tasks.
 
本实验中，完全使用图像作为输入来训练智能体，不依赖于任何的环境数据和机器人数据。在Google PlaNet的基本结构上进行了调整，使其兼容于我们开发的环境。

## Intallation
本实验使用的环境是我的另一个文件夹中创建的环境，请看：
https://github.com/wq13552463699/UR5E_robot_gym_env_Real_and_Sim/tree/main/Simulation
请直接克隆这个文件夹中的容，并将所有文件夹中的文件与此文件夹中的文件放在同一目录下。
其他
pip install -r requirements.txt 

## Result
在经过了500个回合左右的训练，机械手臂基本已经学会了reaching target，请看视频：。。。。。。。

Loss curves:
在reward上，由于我使用的是自定义的reward function（goal-based reward function），得分不固定，你可以想象成每一个分值在300左右的回合都是成功的回合，所以图中最开始
智能体很少能达到target，在经过了击败400回合的训练之后，很少失败。成功率大概在95%以上


##Further Concern:
直接使用图像作为输入有以下的弊端：
纬度高，收敛速度慢。
图像数据中存在大量的冗余信息和噪声，会造成误导。
图像中有很多的潜在信息以待挖掘。
我们需要开发一个完备的representation模型，以克服以上的问题。详情请见我的另一个文件夹。。。。

## Reference
https://github.com/openai/gym
https://github.com/openai/mujoco-py
https://github.com/Kaixhin/PlaNet