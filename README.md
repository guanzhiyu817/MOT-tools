# MOT-tools

## Installation

Step1. Install MOT-tools.
```shell
git clone https://github.com/guanzhiyu817/MOT-tools.git
cd MOT-tools
pip3 install -r requirements.txt
python3 setup.py develop
```

Step2. Install [pycocotools](https://github.com/cocodataset/cocoapi).

```shell
pip3 install cython; pip3 install 'git+https://github.com/cocodataset/cocoapi.git#subdirectory=PythonAPI'
```

Step3. Others
```shell
pip3 install cython_bbox
```

## Data preparation  
  
Download [MOT17](https://motchallenge.net/data/MOT17/), [MOT20](https://motchallenge.net/data/MOT20/) and put them under <MOT-tools>/datasets in the following structure:  
```  
datasets  
|——————MOT17  
| └——————train  
| └——————test  
└——————MOT20  
| └——————train  
| └——————test  
```

## Tools
### convert_mot17_to_coco.py
Converting MOT17 dataset to coco format
```shell  
python3 tools/convert_mot17_to_coco.py
``` 
### convert_mot20_to_coco.py
Converting MOT20 dataset to coco format
```shell  
python3 tools/convert_mot20_to_coco.py
``` 
### convert_video.py
Use the video xxx.mp4 to get xxx_converted.mp4, the new video file has the same size and frame rate as the original video
```shell  
python3 tools/convert_video.py
```
### interpolation.py
Evaluation of object tracking results and interpolation of trajectories
```shell
python tools/interpolation.py
```
### mota.py
Evaluation of tracking results
### trt.py
Converting Pytorch Models to TensorRT Models
```shell
python tools/trt.py -c best_ckpt.pth.tar
```
### txt2video.py
There are two functions, txt2img and img2video, which convert a text file containing ground-truth information into an image, and the resulting image sequence into a video file, respectively
```shell
python tools/txt2video.py
```

