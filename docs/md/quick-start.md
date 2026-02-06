# 快速开始

## 安装
### 环境要求
- **操作系统** : Windows 10+ (64位)
- **GPU** : 支持 OpenGL 3.3+

### 获取程序
TODO

### 运行源代码
- 需安装 [Git](https://git-scm.com/install/) 和 [Python](https://www.python.org/downloads/) 。
- Python 版本: 3.13+

1. **克隆仓库**
```shell
git clone https://github.com/Bychuhan/RePyPhiRenderer.git
cd RePyPhiRenderer
```

2. **安装依赖库**
```shell
pip install uv
uv sync
```

3. **运行**
```shell
uv run python -m src.main
```

### 安装依赖
#### FFmpeg
- 在[此页面](https://github.com/BtbN/FFmpeg-Builds/releases/tag/latest)下载 FFmpeg。
- 解压下载的压缩包，选择一种方式安装。

##### 设置环境变量 (推荐)
将 ffmpeg.exe 所在的目录 (bin文件夹) 添加到系统环境变量的 Path 中。

##### 放置于软件安装目录 (备选)
将 ffmpeg.exe 所在的目录 (bin文件夹) 中所有文件复制到 RePyPR 安装的目录。

## 播放谱面
运行主程序后，会依次弹出谱面、音乐、曲绘的文件选择框。  

目前支持以下谱面格式:
- Phigros 官谱格式 ( `*.json` )
