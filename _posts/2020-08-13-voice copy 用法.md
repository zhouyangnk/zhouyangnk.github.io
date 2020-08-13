### 环境

export PATH=/mnt/lustre/aifs/home/zhx65/tools/miniconda/envs/tf/bin/:$PATH

### 降噪
若录音明显含燥需降噪，可使用默认工具/mnt/lustre/aifs/users/yz312/yanshixitong/without-training-xvector/rnnoise， 或者任何其他降噪工具

### 提特征等
参考下面命令提示操作

female `python /mnt/lustre/aifs/users/yz312/yanshixitong/without-training-xvector/demo/female/train.py --help`

male `python /mnt/lustre/aifs/users/yz312/yanshixitong/without-training-xvector/demo/male/train.py --help`




### 合成
参考下面命令提示操作

female `python /mnt/lustre/aifs/users/yz312/yanshixitong/without-training-xvector/demo/female/syn.py --help`

male `python /mnt/lustre/aifs/users/yz312/yanshixitong/without-training-xvector/demo/male/syn.py --help`

注意：-p参数指定的文件夹只会保存-i参数指定的input文件中第一句合成音频，所有的合成音频在-w参数中指定的文件夹中

### 完整例子

```shell
export PATH=/mnt/lustre/aifs/home/zhx65/tools/miniconda/envs/tf/bin/:$PATH
cd /mnt/lustre/aifs/users/yz312/yanshixitong/without-training-xvector/demo/male
python train.py -a yixin/audio/ -w yixin/train/
Python syn.py -w yixin/train/ -i input -p yixin/output
ls yixin/train/*.wav

```
