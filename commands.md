```
CUDA_VISIBLE_DEVICES=0 torchrun code/train_mdc.py  -dd /mnt/Windows/cv_projects/Dual-Stream-MHSI/dataset/train_val_test_blood.json -r /mnt/Windows/cv_projects/SpecTr/HyperBlood -dh data -dm anno -b 1 -spe_c 128 -b_group 32 -link_p 0 0 1 0 1 0 -sdr 4 4 -hw 160 160 -msd 4 4 -name Dual_MHSI_2 -me 'npz' -et '.float' -c 9
```

```
CUDA_VISIBLE_DEVICES=0 torchrun code/train_mdc.py  -dd /mnt/Windows/cv_projects/Dual-Stream-MHSI/dataset/train_val_test.json -r /mnt/Windows/cv_projects/MHSI_Original/MHSI -dh MHSI/MHSI -b 1 -spe_c 60 -b_group 15 -link_p 0 0 1 0 1 0 -sdr 4 4 -hw 320 256 -msd 4 4 -name Dual_MHSI
```

**b_group** has to equal to **spe_c** / **msd[0]**