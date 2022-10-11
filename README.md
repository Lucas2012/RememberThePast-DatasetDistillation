# Remember The Past - Dataset Distillation &nbsp;&nbsp;

The official implementation of NeurIPS'22 paper: Remember the Past: Distilling Datasets into Addressable Memories for Neural Networks

## Highlights:

## Installation

## Training & testing
Back-propagation through time (BPTT) without memory addressing

```
bash run_scripts/bptt_efficient_compressor_minibatch.sh debug ConvNet compressors_bptt_interventions.yml 1 150 SGD 0.9 CIFAR10 10 10 1 1 none 0
```

Back-propagation through time (BPTT) with memory addressing

```
bash run_scripts/bptt_efficient_compressor_basis_minibatch.sh debug ConvNet compressors_bptt_test.yml 1 SGD 150 SGD 0.9 CIFAR10 10 32 16 2 0 1 1 l2 1e-4 none 0
```

To add data augmentations, change none to flip_rotate

The hyperparameters are tuned with validation_ratio=0.1. When set as 0, the training will use the test set directly.

## Reference
@article{deng2022remember,
  title={Remember the Past: Distilling Datasets into Addressable Memories for Neural Networks},
  author={Deng, Zhiwei and Russakovsky, Olga},
  journal={arXiv preprint arXiv:2206.02916},
  year={2022}
}
