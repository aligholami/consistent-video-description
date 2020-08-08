# consistent-video-description
This is the repository for my experiments on the consistent video description project. The codebase is heavily borrowed from the grounded video description repository.

## Re-running the GVD experiments
1. GVD without Self-Attention with Visdom Monitoring  
```
python main.py --path_opt cfgs/anet_res101_vg_feat_10x100prop.yml --batch_size 16 --cuda --checkpoint_path save/gvd_01 --language_eval --w_att2 0.05 --w_grd 0 --w_cls 0.1 --obj_interact --enabled_visdom --densecap_verbose | tee log/gvd_01
```

You can disable the Visdom by ignoring the `enabled_visdom` flag. Also, self-attention can be disabled by removing the `--obj_interact` flag.