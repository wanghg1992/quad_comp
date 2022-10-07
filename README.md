# **Compare different algorithm for quadruped**
# 1. introduction
## 1.1 classic control
- plan: body trajectory optimization(TO)
- control: optimized whole body control with null space projection(OP-NSP-WBC)
- dynamic: pinocchio
- optimal problem solver: casadi

## 1.2 reinforce learning
- algorithm: ppo
    - input: robot states
    - output: foot velocity

## 1.3 visualization
- rviz
    - urdf: robot
    - trajectory: body, foot
    - point: body, foot, zmp
    
# 2. install
## 2.1 dependency
- install anaconda, and new python3.7 environment naming py37
- install gym: pip3 install gym
- install pybullet: pip3 install pybullet
- install baseline: pip3 install baselines
## 2.2 install gym-quad-env
```shell script
- git clone git@github.com:wanghg1992/quad_comp.git --recurse-submodules
- cd quad_comp/
- pip3 install -e simulation_environment/
```

# 3. run
## 3.1 run classic control
roscore\
./run_classic_control.sh
## 3.2 run rl train
roscore\
./run_baseline_ppo.sh
## 3.3 run visualization
roscore\
./run_visualization.sh
## 3.4 test simulation environment
roscore\
./test_simulation.sh