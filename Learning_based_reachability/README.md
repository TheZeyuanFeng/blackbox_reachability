## Learning-based methods

### Quick Start <br>
Under the "Learning_based_reachability" folder, create conda environment using 
```
conda create --name bb_reach --file requirement.txt
```
Install pytorch
```
pip install torch==2.0.0 torchvision==0.15.1 torchaudio==2.0.1 --index-url https://download.pytorch.org/whl/cu118
```

### Slip-Wheel Car Example
To run our method, you can simply run following command under "Learning_based_reachability" folder:
```
conda activate bb_reach
bash ./scripts/train_ham_method_car.sh
```

### Quadruped Example
1. Set up [Rapid Localmotion via RL](https://github.com/Improbable-AI/rapid-locomotion-rl/tree/main) code under "blackbox_reachability" folder.
2. Replace "legged_robot.py" and "velocity_tracking_easy_env.py" in **Rapid Localmotion via RL** with the files at "data/data_collection_quadruped/". (Coming soon: we will provide a proper git patch file soon.)
3. Run following command under "Learning_based_reachability" folder to get results for Ham-NN:
```
conda activate bb_reach
bash ./scripts/train_ham_method_quadruped.sh
```
4. If you want to train and test all baseline methods
```
bash ./scripts/run_all_baselines_quadruped.sh
```

### (Coming soon) 
A brief tutorial for creating your own examples...