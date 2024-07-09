# KITTI odometry evaluation tool
1. 分清tum与kitti
- tum
timestamp tx ty tz qx qy qz qw
- kitti
r11 r12 r13 tx r21 r22 r23 ty r31 r32 r33 tz
r11,r12,r13,r21,r22,r23,r31,r32,r33 是旋转矩阵的元素。
tx,ty,tz 是平移向量。
2. evo评价 （tum）
- 编写代码输出轨迹
- 统一度量
- tum转kitti
evo_traj tum 06_pred --save_as_kitti
- evo评价kitti 必须轨迹数量必须一样

3. kitti评价
- 下载工具箱
- 评价测试
- python evaluation.py --result_dir=./data/ --eva_seqs=06_pred
