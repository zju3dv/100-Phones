# 100-Phones: A Large VI-SLAM Dataset for Augmented Reality Towards Mass Deployment on Mobile Phones
In this work, we propose 100-phones, a large VI-SLAM dataset consisting of 350 sequences collected by 100 different models of phones. The sensor characteristics among these 100 phone models vary greatly, posing unprecedented challenges for VI-SLAM methods. 

<video src="./assets/100-Phones.mp4"></video>

## Dataset format

### "circle"/ "line"/"rotation"

We design three simple yet typical motions to collect three sub-datasets in a small-scale scene. Each sub-dataset contains 100 sequences collected by the 100 phones. We organize the three sub-dataset as follow and we name the data format as "dior".

> circle-dior/line-dior/rotation-dior
>
> |-- aquos-sense4-lite (phone-model)
>
> ​    |-- camera
>
> ​        |-- sensor.yaml
>
> ​        |-- data.csv
>
> ​        |-- images
>
> ​            |-- 1872301340041.jpg
>
> ​            |-- 1872334665406.jpg
>
> ​            |-- ...
>
> ​    |-- imu
>
> ​        |-- sensor.yaml
>
> ​        |-- data.csv
>
> ​    |-- htc ( HTC SteamVR Tracking 2.0)
>
> ​        |-- sensor.yaml
>
> ​        |-- data.csv
>
> ​    |-- groundtruth
>
> ​        |-- sensor.yaml
>
> ​        |-- data.csv
>
> ​        |-- euroc_gt_body.csv
>
> |-- ...

### "general"

We design the fourth sub-dataset in three large-scale scenes. We select five phones, each collects ten sequences, resulting in 50 sequences. For the "general" sub-dataset, we arrange the data according to five different phone models. Every phone model contains ten sequences of different motions. We organize the "general" sub-dataset as follow:

> general
>
> |-- huawei-mate30-pro (phone-model)
>
> ​    |-- 2022-11-21-11-45-19-465-normal-walk-f1 (sequence-name)
>
> ​	    |-- camera
>
> ​		    |-- sensor.yaml
>
> ​		    |-- data.csv
>
> ​			|-- images
>
> ​                |-- 76204892580000.jpg
>
> ​                |-- 76204926193000.jpg
>
> ​                |-- ...
>
> ​        |-- imu
>
> ​             |-- sensor.yaml
>
> ​             |-- data.csv
>
> ​        |-- groundtruth
>
> ​             |-- euroc_gt_body.csv
>
> ​    |-- 2022-11-21-12-26-08-733-walk-forward-backward-f1 (sequence-name)
>
> ​        |-- ...
>
> |-- vivo-iqoo-7 (phone-model)
>
> ​    |-- ...
>
> | -- ...  

### For ROS

We also provide  the corresponding  bags for VI-SLAM systems that based on ROS. "circle-raw-bag"、“line-raw-bag” and "rotation-raw-bag" contain the raw IMU and image messages.  "circle-sync-bag"、“line-sync-bag” and "rotation-sync-bag" contain the synchronized IMU and image messages with the offline calibrated time offset. Each directory contains bags for 100 model of phones corresponding to the respective motion mode.

For the "general" sub-dataset, "general-raw-bag" and "general-sync-bag" would be also provided and we organized the bags  the same way as before.

## Citation

If you find this code useful for your research, please use the following BibTeX entry.

```bibtex
@article{sun2021loftr,
  title={{LoFTR}: Detector-Free Local Feature Matching with Transformers},
  author={Sun, Jiaming and Shen, Zehong and Wang, Yuang and Bao, Hujun and Zhou, Xiaowei},
  journal={{CVPR}},
  year={2021}
}
```

## Copyright

This work is affiliated with ZJU-SenseTime Joint Lab of 3D Vision, and its intellectual property belongs to SenseTime Group XR.

```
Copyright SenseTime. All Rights Reserved.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

