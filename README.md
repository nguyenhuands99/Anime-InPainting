Anime-InPainting: An demo application of based on [Edge-Connect](https://github.com/knazeri/edge-connect) (WIP)
---------------------------------------------------------------------------------------------------------------

English | [中文版介绍](#jump_zh)     

## Demo show time 🏳️‍🌈
#### Outputs
<p align="center">
<img src="files/show1.jpg" width="720" height="400">
</p>

#### Demo
<p align="center">
<img src="files/cut2.gif" width="425" height="425">
<img src="files/cut3.gif" width="406" height="222">
</p>

Introduction:
-----
This is an optimized demo application which has a frontend based on `Opencv`, whose backend used [Edge-Connect](https://github.com/knazeri/edge-connect).
Make sure you have read their awesome work and license thoroughly.
Compared with the original work, this project has such <span id="improve">improvements</span> :
- Add demo application modes
- Optimize the training phase
  - Auto-save and auto-load latest weights files
  - Add a fast training phase combined with origin phase 2 and 3
- bugs fixed (most of them are merged into the original work)
- Add utility files
- Add configs in `config.yml`
  - PRINT_FREQUENCY
  - DEVICE : cpu or gpu
- ... ...

**You can do the amazing Anime inpainting conveniently here.**

**And detailed training tutorial is introduced below.**

## <span id='pre'>Prerequisites</span>
- Python 3
- PyTorch `1.0` (`0.4` is not supported)
- NVIDIA GPU + CUDA cuDNN

## <span id='ins'>Installation</span>
- Clone this repo
- Install PyTorch and dependencies from http://pytorch.org
- Install python requirements:
```bash
pip install -r requirements.txt
```

## Run the demo
I want to run the demo! Calm down and follow such step:
**Info: The following weights files are trained on anime face dataset which performs not good on a large whole anime character.**
1. Download the well trained model weights file --> [Google Drive](https://drive.google.com/file/d/12I-K7GQEXEL_rEOVJnRv7ecVHyuZE-1-/view?usp=sharing) | [Baidu](https://pan.baidu.com/s/1WkeRtYViGGGw4fUqPo3nsg)
2. Unzip the `.7z` and put it under your root directory
So make sure your path now is: `./model/getchu/<xxxxx.pth>`
3. Complete the above [Prerequisites](#pre) and [Installation](#ins)
4. (Optional) Check and edit the `./model/getchu/config.yml` config file as you wish
5. Run the cooool demo:

#### Default demo:

```bash
python demo_patch.py --path model/getchu/
```

#### Demo with edge window:

```bash
python demo_patch.py --edge -path model/getchu/
```

#### Args help
```bash
python demo_patch.py -h
```

> PS. You can run any well trained model, not only above one. You can download more model weights files
from the original work [Edge-Connect](https://github.com/knazeri/edge-connect). Then you can run the demo as above.
Only one thing to be careful: The `config.yml` in this project has some additional options than the config from the [Edge-Connect](https://github.com/knazeri/edge-connect).


## Demo operation
Refer to your `terminal` prints or refer to the `__doc__` in `demo_patch.py`.

## Training manual


> continuous...

<span id="jump_zh">中文版介绍🇨🇳 (WIP)</span>
-----

## 简介
Demo效果看上面👆 Bilibili视频教程：TO DO

这是图像修补方向最新研究成果[Edge-Connect](https://github.com/knazeri/edge-connect)的~~阿姆斯特朗氮气加速魔改~~（优化）版。
用`Opencv`写了个前端部分，后端是[Edge-Connect](https://github.com/knazeri/edge-connect)，方便当作工具使用。
此工具可以用来自动图像修补，去马赛克……同样优化了模型训练的过程。具体优化内容请看[英文版](#improve)。

## 基础环境
- Python 3
- PyTorch `1.0` (`0.4` is not supported)
- NVIDIA GPU + CUDA cuDNN

## 第三方库安装
- Clone this repo
- Install PyTorch and dependencies from http://pytorch.org
- Install python requirements:
```bash
pip install -r requirements.txt
```

## 运行Demo
教练！我有个大胆的想法🈲……别急，一步步来：
**注意：以下模型是在动漫头像数据集上训练的，所以对动漫全身大图修补效果一般，想自己再训练的参考下面的训练指南**
1. 下训练好的模型文件 --> [Google Drive](https://drive.google.com/file/d/12I-K7GQEXEL_rEOVJnRv7ecVHyuZE-1-/view?usp=sharing) | [Baidu](https://pan.baidu.com/s/1WkeRtYViGGGw4fUqPo3nsg)
2. 解压 `.7z` 放到你的根目录下
确保你的目录现在是这样: `./model/getchu/<xxxxx.pth>`
3. 完成上面的基础环境和第三方库安装步骤
4. (可选) 检查并编辑 `./model/getchu/config.yml` 配置文件
5. 使用以下命令运行：

#### 默认Demo:

```bash
python demo_patch.py --path model/getchu/
```

#### 带Edge编辑窗口的Demo:

```bash
python demo_patch.py --edge -path model/getchu/
```

#### 命令行参数帮助
```bash
python demo_patch.py -h
```

> PS. 你也能用Demo跑别的任何模型，在这里下载原作更多模型[Edge-Connect](https://github.com/knazeri/edge-connect).
文件组织方式参考上面，其余运行命令都一样。唯一注意的是这个项目的 `config.yml` 比原作的多了几个选项，报错了的话注意修改。

## Demo操作指南
详细内容请翻看控制台的打印内容，或查看`demo_patch.py`里的`__doc__`      
简略版Demo使用：

按键 | 说明
-----|------
按键 `[` | 笔刷变细 （控制台打印粗细大小）
按键 `]` | 笔刷变粗
按键 `0` | Todo
按键 `1` | Todo
按键 `n` | 修补黑色涂抹区域，只使用一张输入图片
按键 `e` | 修补黑色涂抹区域，使用输入图片和边缘图片（仅当edge窗口启动时有效）
按键 `r` | 全部重置
按键 `s` | 保存输出图片
按键 `q` | 退出


## 训练指南

> continuous...


## License
Licensed under a [Creative Commons Attribution-NonCommercial 4.0 International](https://creativecommons.org/licenses/by-nc/4.0/).

Except where otherwise noted, this content is published under a [CC BY-NC](https://creativecommons.org/licenses/by-nc/4.0/) license, which means that you can copy, remix, transform and build upon the content as long as you do not use the material for commercial purposes and give appropriate credit and provide a link to the license.


## Citation
If you use this code for your research, please cite our paper <a href="https://arxiv.org/abs/1901.00212">EdgeConnect: Generative Image Inpainting with Adversarial Edge Learning</a>:

```
@inproceedings{nazeri2019edgeconnect,
  title={EdgeConnect: Generative Image Inpainting with Adversarial Edge Learning},
  author={Nazeri, Kamyar and Ng, Eric and Joseph, Tony and Qureshi, Faisal and Ebrahimi, Mehran},
  journal={arXiv preprint},
  year={2019},
}
```

