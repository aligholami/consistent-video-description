# consistent-video-description
This is the repository for my experiments on the consistent video description project. The codebase is heavily borrowed from the grounded video description repository.

## Preparing the Environment
TBD.
## Re-running the GVD experiments
1. Training GVD without Self-Attention with Visdom Monitoring  
```
python main.py --path_opt cvd/cfgs/anet_res101_vg_feat_10x100prop.yml --batch_size 16 --cuda --check
point_path experiments/save/gvd_01 --language_eval --w_att2 0.05 --w_grd 0 --w_cls 0.1 --obj_interact --enable_visdom --densecap_verbose | tee experiments/log/gvd_01
```
Make sure you have the desired name instead of `gvd_01`. Also, make sure to have a running Visdom server by running `visdom` in a different bash session. You can disable the Visdom by ignoring the `enabled_visdom` flag. Also, self-attention can be disabled by removing the `--obj_interact` flag.