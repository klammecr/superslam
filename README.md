# SuperSLAM

SLAM with deep learning feature and descriptors (SuperPoint)

This work includes changing the ORB-SLAM2 pipeline in order to work with deep learning descriptors like SuperPoint. Eventually, we would like to use SuperGlue to improve matching even further in this pipeline

Docker Container: [superslam](https://hub.docker.com/r/cklammer/superslam)

```
docker pull cklammer/superslam
```

Code for Superpoint v2 (Superpoint-opt) which is vanilla SuperPoint with a MobileNet backbone and support for both RGB and Grayscale inputs:
[Superpoint-opt](https://github.com/thebharathsk/superpoint-optimized)

## Vocabularies:
[Superpoint v1 Vocabulary](https://drive.google.com/file/d/1M_SjdDFACHFl8CN6CchaRM_puHhqTUwl/view?usp=sharing)
[Superpoint v2 Vocabulary](https://drive.google.com/file/d/1R4juBr5f5Qcm-NeirsMDB0B3mZnjFbld/view?usp=sharing)

## Project Contributions:
- [X] Docker container to work with deep learning descriptors and setting environment
- [X] Support with DBoW3 and C++17 thanks to GCN_v2's repo
- [X] Fixing bugs in code with regard to loop closures and tracking from the community
- [X] Improve QoL when using standard library
- [X] Training a vocabulary for Superpoint and a MobileNet variant Superpoint_v2
- [X] Reworking matching to work with deep learning descriptors, adding nearest neighbor matching from GCN_v2's repo
- [X] Easier data pipelining with datasets like TartanAir and TUM

Look to see additional improvements coming soon!

## Schedule for Upcoming Work:
| Status | Target Completion | Contribution |
| :---        |    :----:    |          :---: |
| &#9745;  | **End May**       | Include trained vocabularies used for Superpoint_v1 and Superpoint_v2 and shell scripts used to pull them down|
| In Progress....  | **End May-Begin June** | Investigate performance issues for Superpoint v1 
| &#9744;  | **?**   | Validate all code is migrated and switch over docker image to have the latest pre-loaded |
| &#9744;  | **?**      | Integrating our Superpoint_v2 (Superpoint-opt) into this repo|
| &#9744;  | **?**     | Adding a switch allowing use of both ORB and Superpoint frontends|
| &#9744;  | **?**  | Speed up and better acceleration for GPUs |
| &#9744;  | **?**    | Adding SuperGlue/GCN/COTR for matching |
| &#9744;  | **?**    | Begin summarizing and finalizing work and findings for a workshop/conference |
