# lidar_feature_matching
Implementing a simple framework for learning 3D keypoint descriptors that can be used for sparse point cloud registration. The framework consists of:

1) A simple network (e.g., pointnet) for extracting per-point descriptors for all points within a point cloud (assume the point cloud is highly downsampled for now)
2) A differentiable keypoint matcher (use the differentiable Sinkhorn-Knopp algorithm from SuperGlue)
3) A differentiable bundle adjustment algorithm (in this case, we assume 3D points are accurate, so only optimize for the pose between two point clouds)
4) A keypoint matching loss (a contrastive loss) and a pose loss

Will be following the WandB introductory MLOps course. 

## Steps:

- [ ] Acquire a dataset (preferably an AV dataset, only train using single scans
- [ ] Set up pytorch training dataloader (use single scans, and generate a second cloud by transforming with a known pose)
- [ ] Exploratory data analysis in W&B
- [ ] Get basic network architecture
- [x] Set up Sinkhorn-Knopp algorithm for keypoint matching (test with SIFT)
- [ ] Implement contrastive matching loss
- [ ] Implement differentiable pose optimizer (2D, solves for translation and yaw angle)
- [ ] Network training experiments
- [ ] Model evaluation
