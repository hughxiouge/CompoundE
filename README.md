# CompoundE

Code for "CompoundE: Knowledge Graph Embedding with Translation, Rotation and Scaling Compound Operations"

## OGB installation

https://github.com/snap-stanford/ogb

#### Recommended order of installation 
 - Create a python 3.8.8 environment using Anaconda
 - Install torch 1.11.0 using Anaconda
 - Install torch-geometric using Anaconda
 - Install ogb using pip
 - Install other packages using pip

## After installing the OGB environment, to reproduce the results

```
CUDA_VISIBLE_DEVICES=0 python run.py --do_train --cuda --do_valid --do_test --evaluate_train \
            --model CompoundE -n 250 -b 4096 -d 100 -g 7 -a 1.0 -adv -tr \
            -lr 0.005 --max_steps 300000 --cpu_num 8 --test_batch_size 32  --print_on_screen
```

## Acknowledgement
We refer to the code of [PairRE](https://github.com/alipay/KnowledgeGraphEmbeddingsViaPairedRelationVectors_PairRE). Thanks for their contributions.

**Citation**

If you find the source codes useful, please consider citing our [paper](https://arxiv.org/abs/2207.05324):

```
@article{ge2022compounde,
  title={Compounde: Knowledge graph embedding with translation, rotation and scaling compound operations},
  author={Ge, Xiou and Wang, Yun-Cheng and Wang, Bin and Kuo, C-C Jay},
  journal={arXiv preprint arXiv:2207.05324},
  year={2022}
}
```