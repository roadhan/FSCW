# FSCW

This repository contains the code (in PyTorch) for the paper:
See you somewhere in the ocean: Few-shot domain adaptive underwater object detection

The code of this repository is based on: https://github.com/ultralytics/yolov5

Our demo is based on :https://www.youtube.com/watch?v=PfEz7yE4m0U

### Dependencies

- Python 3.7
- PyTorch >=1.7
- CUDA11.0 and cuDNN
- numpy
- tqdm
- tensorboardX

### Dataset

urpc  链接：https://pan.baidu.com/s/1QcTsP62KQcEiB831cGimRw 

      提取码：7eym
      
aquarium https://universe.roboflow.com/data-science-day-dry-run/aquarium-6cfzm/dataset/1

### Sourcedomaintrain 
python train.py --data crossdomain.yaml --epochs 300 --weights yolov5x.pt --cfg yolov5x_CS.yaml

### Targetdomaintrain 
python trainfreeze.py --data aquam.yaml --epochs 300 --weights your_source_trained_weight_path --cfg yolov5x_CS.yaml
