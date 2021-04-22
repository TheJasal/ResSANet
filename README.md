# ResSANet

## Usage: Preparation

- Requirement

  - Ubuntu 16.04
  - Python 3 (recommend Anaconda3)
  - Pytorch 0.3.\*
  - CMake > 2.8
  - CUDA 8.0 + cuDNN 5.1

- Building Kernel

      git clone https://github.com/Yochengliu/DensePoint.git 
      cd DensePoint
      mkdir build && cd build
      cmake .. && make

- Dataset
  - Shape Classification: download and unzip [ModelNet40](https://shapenet.cs.stanford.edu/media/modelnet40_ply_hdf5_2048.zip) (415M). Replace `$data_root$` in `cfgs/config_cls.yaml` with the dataset parent path.

## Usage: Training
- Shape Classification

      sh train_cls.sh
        
We have trained a 6-layer classification model in `cls` folder, whose accuracy is 92.38%.

## Usage: Evaluation
- Shape Classification

      Voting script: voting_evaluate_cls.py
        
You can use our model `cls/model_cls_L6_iter_36567_acc_0.923825.pth` as the checkpoint in `config_cls.yaml`, and after this voting you will get an accuracy of 92.5% if all things go right.

## License

The code is released under MIT License (see LICENSE file for details).

## Acknowledgement

The code is heavily borrowed from [Densepoint](https://github.com/Yochengliu/DensePoint).
        
## Contact

If you have some ideas or questions about our research to share with us, please contact <zheng-zh18@mails.tsinghua.edu.cn>
