# SuperSLAM

SLAM with deep learning feature and descriptors (SuperPoint)

This work includes changing the ORB-SLAM pipeline in order to work with deep learning descriptors like SuperPoint. Eventually, we would like to use SuperGlue to imporve matching even further in this pipeline

Docker Container: `https://hub.docker.com/r/cklammer/superslam`

```
docker pull cklammer/superslam
```

Contributions:
- [X] Docker container to work with deep learning descriptors and setting environment
- [X] Support with DBoW3 and C++17 thanks to GCN_v2's repo
- [X] Fixing bugs in code with regard to loop closures and tracking from the community
- [X] Improve QoL when using standard library
- [X] Training a vocabulary for Superpoint and a MobileNet variant Superpoint_v2
- [X] Reworking matching to work with deep learning descriptors, adding nearest neighbor matching from GCN_v2's repo
- [X] Easier data pipelining with datasets like TartanAir and TUM

Look to see additional improvements coming soon!

Future Work:
- [ ] Integrating our Superpoint_v2 into this repo
- [ ] Adding SuperGlue for matching
- [ ] Speed up and better acceleration for GPUs
