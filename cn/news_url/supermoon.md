```
# SuperMoon: A pytorch library for hypergraph learning.
**SuperMoon** is a python toolbox for hypergraph-based deep learning, which is built upon [pytorch](https://pytorch.org/). 
 Edge in hypergraph named hyperedge can link more than two nodes, which allows hyperedge to express more than pair-wise 
 relation(like: entity-attribute relation, group relation, hierarchical relation and so on.). Thus, hypergraph owns more 
 powerful model ability than common graph. 
 
 It consists of sparse hypergraph construction, fusion, convolution operations, convenient util functions for medical
 image(MRI, Pathology, etc.), 3D(point cloud, view-based graph, etc.) and other hypergraph applications(to be continue...).
 Hypergrpah inductive learning and hypergraph transductive learning examples is also included in this toolbox. What's more,
 we write several examples that deploy hypergraph in different tasks like: Classification, Segmentation and Regression.    
 
 The supported operations include: 
 
 * **Hyperedge base operations**: compute hyperedge/node degree, add/remove hypergraph self loop, count hyperedge/node number,
 
 * **Hyperedge construction operations**: construct hyperedge group from grid-like structure (image) with spatial neighbors, 
 construct hyperedge group from feature spatial neighbors. K Nearest Neighbors algorithm is supported here.
 
 * **Hyperedge group/Hypergraph fusion operations**: fusion hypergraphs with concatenate constructed hypergraph incidence matrix.
 
 * **Hypergraph Convolution**: the common hyconv(hypergrpah convolution) ([Feng et al. AAAI2019](https://github.com/iMoonLab/HGNN)) 
 is implemented here.
 
 * **Models**: HGNN([Feng et al. AAAI2019](https://github.com/iMoonLab/HGNN)) with two hyconv layers, ResNet(18, 34, 50, 101, 152)
 ([He et al.](https://arxiv.org/abs/1512.03385)), and ResNet_HGNN a combination of ResNet and HGNN for image input and real-time
 construct hypergraph supported.
 
 * **Utils**: some convenient util functions(to be continue... ):
    * **Data**: multiple modality data supported (to be continue...)
        * **MRI**: mri series read and write functions.
        * **Pathology**: sample patches from WSI slide return patch coordinates(left top point) and patch width and height. 
        draw sampled patches on WSI slide function for overview or visualization.
    * **Meter**: evaluate meters in hypergraph learning.
        * **Inductive**:  *C-Index Meter* for survival prediction.
        * **Transductive**: compute class accuracy in classification task for transductive learning, compute IOU Score for 
        segmentation task in transductive learning. 
    * **Visualization**: some visualization functions.
        * **Transductive**: visualize segmentation result in transductive learning. 


 ## Installation
 Ensure that at least Python3, PyTorch 1.2.0 is installed. HyperG is still under development. Before the first stable 
 release (1.0), please clone the repository and run
 ```commandline
pip install .
 ```

## Documentation
Tutorial and Documentation will coming soon!
    
## Examples
We provide examples in classification, regression, segmentation tasks with hypergraph, for more detail refer to our tutorials.

## Citing THU-SuperMoon
If you find **THU-SuperMoon** is useful in your research, please consider citing:
​```
@inproceedings{feng2019hypergraph,
  title={Hypergraph neural networks},
  author={Feng, Yifan and You, Haoxuan and Zhang, Zizhao and Ji, Rongrong and Gao, Yue},
  booktitle={Proceedings of the AAAI Conference on Artificial Intelligence},
  volume={33},
  pages={3558--3565},
  year={2019}
}
​```

## Contributing
We always welcome contributions to help make HyperG better, and apply hypergraph in more applications. If you would like 
to contribute, please [contact us](mailto:evanfeng97@gmail.com).
```