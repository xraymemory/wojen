# WOJEN

Download the full repo here - https://drive.google.com/file/d/1Ay8_wxmtCdd0EyFpR_hPYkbxXyHNmOYl/view?usp=sharing to get the models and .PTH files

Train using `python train.py --dataroot datasets\wojen --name wojen_pix2pix --model pix2pix --direction BtoA --continue_tran --epoch_count 0 --n_epochs 10000 --display_id 0`

Generate samples with `python test.py --dataroot datsets\wojen\trainB --name wojen_pix2pix --model test --netG unet_256 --direction BtoA --dataset_mode single --norm batch`

To add new data, you must place wojak and face images in their respective directories in .\datasets\wojen\ and make sure they have a corresponding filename (both files named e.g. "420.jpg"). Images must be 360x360. Once you have collected and placed your new images, run `python .\datasets\combine_A_and_B.py --fold_A .\datasets\wojen\A --fold_B .\datasets\wojen\B\ --fold_AB .\datasets\wojen\ --no_multiprocess`
