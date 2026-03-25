# BMLProject

## Repository Contents

### Checkpoints
Checkpoints store the saved weights of the trained neural networks. Four checkpoint files from the final epoch (epoch 30) are included:
- `G_epoch_30.pth` — Generator G (Photo → Monet style)
- `F_epoch_30.pth` — Generator F (Monet → Photo, reverse mapping)
- `D_Y_epoch_30.pth` — Discriminator D_Y (judges Monet images)
- `D_X_epoch_30.pth` — Discriminator D_X (judges Photos)

These can be loaded directly to run inference without retraining the model.

### Outputs
The `outputs/` folder contains results generated during and after training:
- `sample_epoch_001.png` through `sample_epoch_030.png` — side-by-side comparisons of a real photo, its Monet-style output, and the cycle-reconstructed photo, saved at the end of every training epoch to track visual progress
- `training_loss_curves.png` — plots of generator loss, discriminator loss, cycle consistency loss, identity loss, and learning rate across all 30 epochs
- `inference_grid.png` — a grid showing 6 random photos alongside their Monet-style translations, generated after training
- `my_monet.png` — Monet-style version of `my_pic.jpg`
- `comparison_my_monet.png` — side-by-side comparison of the original photo and its Monet output

### Sample Images
- `my_pic.jpg` — a personal photo used to test the trained model
- `output_image_128x128.jpg` — personal photo converted to 128×128 resolution, used to test the trained model
