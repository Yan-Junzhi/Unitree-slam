# Unitree-slam
To solve the problem that Unitree A1 dog can not move when you have set the 2d nav goal on the map.
The reason is that some data sended by lcm is not cmd needed, for example, lcm send forwardSpeed but cmd need velocity[0]. Therefore, change the data name of forwardSpeed can solve this problem.
Firstly, replace comm.h in slam_planner_sdk\include\unitree_legged_sdk.
Secondly, alter the data name that need to change in slamplanner\include\slam_planner\convert.h, like lcm.forwardSpeed.
Then catkin_make your work space.
Finally,your dog can move!

