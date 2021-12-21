# GPU_scheduler
#### To change the Period and Deadline :
- For RRT change the TCB parameter in RRT/rrt.cu inside the function init_rrt()
- For Depth Estimation change the TCB parameter in darknet/src/classifier.c inside the function depth_estimation_init()
- For Depth Estimation change the TCB parameter in darknet/src/detector.c inside the function object_detection_init()

#### To execute the scheduler with static priority with all three tasks
- ./TEST_SCHED static -p 3 -o 2 -d 1
- -p is for path planning, -o is of object detection, -d if for depth estimation

#### To execute the scheduler with dynamic priority with all three tasks
- ./TEST_SCHED dynamic

#### To use scheduler for other CNN models
 - Use the convert_weights_file.ipynb to convert the weights from pytorch framework to darknet framework
 - create cfg file for the CNN model, copy the cfg file in darknet/cfg folder
 - Copy the weights file in darknet/weights folder
