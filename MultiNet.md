# 1. Clone repository.
```shell
$ git clone https://github.com/MarvinTeichmann/MultiNet.git
$ git submodule update --init --recursive
$ cd submodules/KittiBox/submodules/utils/ && make
$ cd submodules/KittiBox/submodules/KittiObjective2/ && make
```
---

# 2. run MultiNet.
```shell
# run demo.py
$ python demo_seg\&obj.py --input data/demo/6_8.png
# run train.py
$ python train.py --hypes hypes/multinet2.json
```
---

# 3. File directories.
```shell
MultiNet
├── data
│   ├── demo
│   └── images
├── DATA
│   ├── data_road
│   │   ├── gtFine
│   │   │   ├── train
│   │   │   │   ├── aachen
│   │   │   │   ├── bochum
│   │   │   │   ├── bremen
│   │   │   │   ├── cologne
│   │   │   │   ├── darmstadt
│   │   │   │   ├── dusseldorf
│   │   │   │   ├── erfurt
│   │   │   │   ├── hamburg
│   │   │   │   ├── hanover
│   │   │   │   ├── jena
│   │   │   │   ├── krefeld
│   │   │   │   ├── monchengladbach
│   │   │   │   ├── strasbourg
│   │   │   │   ├── stuttgart
│   │   │   │   ├── tubingen
│   │   │   │   ├── ulm
│   │   │   │   ├── weimar
│   │   │   │   └── zurich
│   │   │   └── val
│   │   │       ├── frankfurt
│   │   │       ├── lindau
│   │   │       └── munster
│   │   ├── leftImg8bit
│   │   │   ├── test
│   │   │   │   ├── berlin
│   │   │   │   ├── bielefeld
│   │   │   │   ├── bonn
│   │   │   │   ├── leverkusen
│   │   │   │   ├── mainz
│   │   │   │   └── munich
│   │   │   ├── train
│   │   │   │   ├── aachen
│   │   │   │   ├── bochum
│   │   │   │   ├── bremen
│   │   │   │   ├── cologne
│   │   │   │   ├── darmstadt
│   │   │   │   ├── dusseldorf
│   │   │   │   ├── erfurt
│   │   │   │   ├── hamburg
│   │   │   │   ├── hanover
│   │   │   │   ├── jena
│   │   │   │   ├── krefeld
│   │   │   │   ├── monchengladbach
│   │   │   │   ├── strasbourg
│   │   │   │   ├── stuttgart
│   │   │   │   ├── tubingen
│   │   │   │   ├── ulm
│   │   │   │   ├── weimar
│   │   │   │   └── zurich
│   │   │   └── val
│   │   │       ├── frankfurt
│   │   │       ├── lindau
│   │   │       └── munster
│   │   ├── testing
│   │   │   ├── calib
│   │   │   └── image_2
│   │   └── training
│   │       ├── calib
│   │       ├── gt_image_2
│   │       └── image_2
│   ├── KittiBox
│   │   ├── testing
│   │   │   └── image_2
│   │   └── training
│   │       ├── image_2
│   │       └── label_2
│   └── weights
├── docu
├── hypes
├── incl
│   ├── tensorflow_fcn -> ../submodules/tensorflow-fcn
│   └── tensorvision -> ../submodules/TensorVision/tensorvision
├── licenses
├── RUNS
│   ├── multinet2_2018_12_15_12.33
│   │   ├── detection
│   │   ├── images
│   │   └── segmentation
│   └── MultiNet_ICCV
│       ├── detection
│       ├── road
│       └── segmentation
└── submodules
    ├── KittiBox
    │   ├── data
    │   │   └── images
    │   ├── decoder
    │   ├── encoder
    │   ├── evals
    │   ├── hypes
    │   ├── incl
    │   │   ├── tensorflow_fcn -> ../submodules/tensorflow-fcn
    │   │   ├── tensorvision -> ../submodules/TensorVision/tensorvision
    │   │   └── utils -> ../submodules/utils
    │   ├── inputs
    │   ├── licenses
    │   ├── optimizer
    │   ├── submodules
    │   │   ├── KittiObjective2
    │   │   │   ├── val_gt
    │   │   │   └── val_pred
    │   │   ├── tensorflow-fcn
    │   │   │   └── test_data
    │   │   ├── TensorVision
    │   │   │   ├── bin
    │   │   │   ├── docs
    │   │   │   │   ├── modules
    │   │   │   │   └── user
    │   │   │   └── tensorvision
    │   │   │       └── tests
    │   │   └── utils
    │   │       ├── annolist
    │   │       ├── hungarian
    │   │       └── kaffe
    │   └── tests
    ├── KittiClass
    │   ├── data
    │   │   ├── demo
    │   │   └── examples
    │   ├── decoder
    │   ├── encoder
    │   ├── evals
    │   ├── hypes
    │   ├── incl
    │   │   ├── tensorflow_fcn -> ../submodules/tensorflow-fcn
    │   │   └── tensorvision -> ../submodules/TensorVision/tensorvision
    │   ├── inputs
    │   ├── optimizer
    │   └── submodules
    │       ├── tensorflow-fcn
    │       │   └── test_data
    │       └── TensorVision
    │           ├── bin
    │           ├── docs
    │           │   ├── modules
    │           │   └── user
    │           └── tensorvision
    │               └── tests
    ├── KittiSeg
    │   ├── data
    │   │   ├── demo
    │   │   └── examples
    │   ├── decoder
    │   ├── docu
    │   ├── encoder
    │   ├── evals
    │   ├── hypes
    │   ├── incl
    │   │   ├── evaluation -> ../submodules/evaluation/
    │   │   ├── seg_utils -> ../submodules/evaluation/kitti_devkit
    │   │   ├── tensorflow_fcn -> ../submodules/tensorflow-fcn
    │   │   └── tensorvision -> ../submodules/TensorVision/tensorvision
    │   ├── inputs
    │   ├── licenses
    │   ├── optimizer
    │   └── submodules
    │       ├── evaluation
    │       │   └── kitti_devkit
    │       ├── tensorflow-fcn
    │       │   └── test_data
    │       └── TensorVision
    │           ├── bin
    │           ├── docs
    │           │   ├── modules
    │           │   └── user
    │           └── tensorvision
    │               └── tests
    ├── tensorflow-fcn
    │   └── test_data
    └── TensorVision
        ├── bin
        ├── docs
        │   ├── modules
        │   └── user
        └── tensorvision
            └── tests
```
