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

Download [MOT17](https://motchallenge.net/data/MOT17/), [MOT20](https://motchallenge.net/data/MOT20/)
, [DanceTrack](https://github.com/DanceTrack/DanceTrack)and put them under <MOT-tools>/datasets in the following
structure:

```  
datasets  
|——————MOT17  
| └——————train  
| └——————test  
└——————MOT20  
| └——————train  
| └——————test
└——————dancetrack        
| └——————train
| └——————val  
| └——————test 
```

## Other datasets


[KITTI](https://www.cvlibs.net/datasets/kitti/eval_tracking.php)

[MOT15](https://motchallenge.net/data/MOT15/)

[MOT16](https://motchallenge.net/data/MOT16/)

[TAO](https://motchallenge.net/data/TAO_Challenge/)

[3D-ZeF](https://motchallenge.net/data/3D-ZeF20)

[CroHD](https://motchallenge.net/data/Head_Tracking_21/)

[SN-Tracking](https://www.soccer-net.org/data)

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

### convert_dance_to_coco.py

Converting DanceTrack dataset to coco format

```shell  
python3 tools/convert_dance_to_coco.py
``` 

### convert_video.py

Use the video xxx.mp4 to get xxx_converted.mp4, the new video file has the same size and frame rate as the original
video

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

There are two functions, txt2img and img2video, which convert a text file containing ground-truth information into an
image, and the resulting image sequence into a video file, respectively

```shell
python tools/txt2video.py
```

# TBD models

[LGMTracker](https://github.com/GaoangW/LGMTracker)

[LPC-MOT](https://github.com/daip13/LPC_MOT)

[GMTracker](https://github.com/jiaweihe1996/GMTracker)

[ByteTrack](https://github.com/ifzhang/ByteTrack)

[OC-SORT](https://github.com/noahcao/OC_SORT)

[GHOST](https://github.com/dvl-tum/GHOST)

[SUSHI](https://github.com/dvl-tum/SUSHI)

# E2E models

[SiamMOT](https://github.com/amazon-science/siam-mot)

[GTR](https://github.com/xingyizhou/GTR)

[TrackFormer](https://github.com/timmeinhardt/trackformer)

[MOTR](https://github.com/megvii-research/MOTR)

[TransCenter](https://github.com/yihongXU/TransCenter)

[TransRMOT](https://github.com/wudongming97/RMOT)

[MOTRv2](https://github.com/megvii-research/MOTRv2)

[MeMOTR](https://github.com/MCG-NJU/MeMOTR)

[ColTrack](https://github.com/bytedance/ColTrack)
