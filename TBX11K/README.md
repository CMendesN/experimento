Paper title: Rethinking Computer-Aided Tuberculosis Diagnosis
Authors: Yun Liu, Yu-Huan Wu, Yunfeng Ban, Huifang Wang, Ming-Ming Cheng


This TBX11K dataset contains 11200 X-ray images with corresponding bounding box annotations for tuberculosis (TB) areas. All images are with a size of 512x512. There are five categories in this dataset, i.e., Healthy, Sick but Non-TB, Active TB, Latent TB, and Uncertain TB. We split this dataset into training, validation, and testing sets, consisting of 6600, 1800, and 2800 X-ray images, respectively. We provide the image lists of the training, validation, and training+validation sets, namely 'TBX11K_train.txt', 'TBX11K_val.txt', and 'TBX11K_trainval.txt', respectively.


Since TB data are very expensive in practice, we take the data from four small TB datasets here to make full use of the existing data. These four datasets are DA, DB, Montgomery, and Shenzhen X-ray datasets, consisting of 156, 150, 138, and 662 X-ray images, respectively. We view a part of each dataset as the training and validation sets, as shown in the folder of 'imgs/extra/'. We combine the rest of the data in these four datasets and our 2800 testing X-rays as the new testing set, as in the list of 'all_test.txt'. We also combine our data with the training/validation X-rays of these four datasets to construct new training, validation, and training+validation sets, namely 'all_train.txt', 'all_val.txt', and 'all_trainval.txt', respectively.


The ground truth of the testing set will not be released, because it is an online competition for computer-aided tuberculosis diagnosis. To promote the development of this field, we suggest you use the 'all_train' set for training and the 'all_val' set for validation when tuning your model. When you submit your results of the testing set to our server, we suggest you training your model on the 'all_trainval' set and testing on the 'all_test' set.


The folder of 'annotations/xml/' contains the bounding box annotations for TB X-rays in the TBX11K 'trainval' set. The folder of 'annotations/json/' contains the [MSCOCO style] json annotation files, which can be generated by running the script of 'code/make_json_anno.sh', i.e., 'sh code/make_json_anno.sh'. Please see the code for more details.


We also define the evaluation metrics for this dataset. Please refer to our paper for more details.


If you use the data here for a publication, please consider citing the following papers:

  # TBX11K dataset
  @inproceedings{liu2020rethinking,
    title={Rethinking computer-aided tuberculosis diagnosis},
    author={Liu, Yun and Wu, Yu-Huan and Ban, Yunfeng and Wang, Huifang and Cheng, Ming-Ming},
    booktitle={IEEE/CVF Conference on Computer Vision and Pattern Recognition},
    pages={2646--2655},
    year={2020}
  }

  # DA and DB datasets
  @article{chauhan2014role,
    title={Role of gist and PHOG features in computer-aided diagnosis of tuberculosis without segmentation},
    author={Chauhan, Arun and Chauhan, Devesh and Rout, Chittaranjan},
    journal={PloS One},
    volume={9},
    number={11},
    pages={e112980},
    year={2014},
    publisher={Public Library of Science}
  }

  # Montgomery and Shenzhen datasets
  @article{jaeger2014two,
    title={Two public chest X-ray datasets for computer-aided screening of pulmonary diseases},
    author={Jaeger, Stefan and Candemir, Sema and Antani, Sameer and W{\'a}ng, Y{\`\i}-Xi{\'a}ng J and Lu, Pu-Xuan and Thoma, George},
    journal={Quantitative Imaging in Medicine and Surgery},
    volume={4},
    number={6},
    pages={475},
    year={2014},
    publisher={AME Publications}
  }
