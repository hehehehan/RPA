# RPA

# Data
We use datasets which are sampled from UCF-101 and Kinetics-400. You can download them from [here](https://drive.google.com/drive/folders/1O4XyLw37WqGKqFvWFaE2ps5IAD_shSpG?usp=sharing).

# Models
We use six pretrained video recognition models on UCF101 and Kinetics-400. You can download them from  [here](https://drive.google.com/drive/folders/10KOlWdi5bsV9001uL4Bn1T48m9hkgsZ2?usp=sharing) and [gluoncv](https://cv.gluon.ai/model_zoo/action_recognition.html), respectively. After downloading the UCF-101 models, you should place them into ./checkpoints.

# other files
You could get other Required files from [**TT**](https://github.com/zhipeng-wei/TT/tree/master)

## Generate adversarial examples.
```
python attack.py/attack_ucf101.py --gpu 0 --batch_size 1 --model slowfast_resnet101 --attack_method TemporalTranslation --step 10 --file_prefix yours --momentum --kernlen 15 --move_type adj --kernel_mode gaussian
```

## Attack Success rate
``` bash
python reference_kinetics.py/reference_ucf101.py --gpu 0 --adv_path your_adv_path
```
* adv_path: name of the output file 


## License
This source code is made available for research purposes only.

## Acknowledgment
Our code is built upon [**TT**](https://github.com/zhipeng-wei/TT/tree/master).

