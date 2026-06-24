# 小目标交通标志智能检测与识别系统

<p>
  <img src="https://img.shields.io/badge/YOLOv12-Ultralytics-orange?style=flat-square" alt="YOLOv12">
  <img src="https://img.shields.io/badge/Django-5.0-green?style=flat-square" alt="Django">
  <img src="https://img.shields.io/badge/Python-3.10+-blue?style=flat-square" alt="Python">
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=flat-square" alt="License">
</p>

> **Tiny Traffic Sign Intelligent Detection and Recognition System** — 基于 YOLOv12 深度学习模型与 Django 框架构建的轻量级交通标志检测与识别平台，支持网页端与移动端部署。

---

## 📌 项目简介

本系统基于 **YOLOv12** 目标检测模型，利用 **TT100K 交通标志数据集** 进行训练，实现对交通场景中**小目标交通标志**的高精度检测与识别，并通过 **Django 框架** 构建后端服务，提供图像上传、实时检测与结果可视化展示的完整流程。

适用于智能交通监控、辅助驾驶系统、道路标志巡检等应用场景。

---

## 🧠 技术栈

| 模块 | 技术选型 |
|------|---------|
| 深度学习模型 | YOLOv12（Ultralytics） |
| 训练数据集 | TT100K（交通标志） |
| 后端框架 | Django 5.0+ |
| 前端 | HTML + Bootstrap |
| 图像处理 | OpenCV + Pillow |
| 模型格式 | PyTorch (.pt) |
| 运行环境 | GPU / CPU 均可 |

---

## 📁 项目结构

```
Tiny-Traffic-Sign-Intelligent-Detection-and-Recognition-System/
├── manage.py                        # Django 管理脚本
├── requirement.txt                  # Python 依赖
├── detector.zip                     # 前端页面组件压缩包
│   └── detector/                     # (解压后) 视图与前端逻辑
│       ├── static/icons/            # 图标与图例资源
│       ├── templates/detector/      # HTML 模板
│       └── views.py                 # 上传与识别视图
├── model.zip                        # 模型与训练脚本压缩包
│   └── model/                       # (解压后)
│       ├── exp_TT100K2/             # 训练好的 YOLOv12 模型权重
│       ├── detect.py                # 图像检测脚本
│       ├── train.py                 # 模型训练脚本
│       └── data.yaml                # YOLO 数据集配置文件
├── traffic_sign_app/                # Django 项目配置
│   └── settings.py, urls.py, ...
├── media/uploads/                   # 用户上传图片存储目录
├── test_image.zip                   # 测试图片集
└── traffic_sign_app.zip             # 完整 Django 应用压缩包
```

---

## 🚀 快速开始

### 1. 克隆项目

```bash
git clone https://github.com/fzk888/Tiny-Traffic-Sign-Intelligent-Detection-and-Recognition-System.git
cd Tiny-Traffic-Sign-Intelligent-Detection-and-Recognition-System
```

### 2. 安装依赖

```bash
pip install -r requirement.txt
```

> 推荐使用国内镜像源加速：
> ```bash
> pip install -i https://pypi.tuna.tsinghua.edu.cn/simple -r requirement.txt
> ```

### 3. 解压资源文件（如需训练或测试）

```bash
unzip detector.zip
unzip model.zip
unzip traffic_sign_app.zip
unzip test_image.zip
```

### 4. 启动服务

**网页端（仅本机访问）：**
```bash
python manage.py runserver
```

**移动端 / 局域网部署：**
```bash
python manage.py runserver 0.0.0.0:8000
# 确保手机与电脑在同一局域网下，访问 http://<电脑IP>:8000/
```

### 5. 访问使用

在浏览器打开 `http://127.0.0.1:8000/`，上传交通场景图片即可获得检测结果。

---

## 📊 模型性能

| 指标 | 数值 |
|------|------|
| mAP@0.5 | ≥ 0.87 |
| mAP@0.5:0.95 | ≥ 0.68 |
| 适用目标 | 小尺寸交通标志（限速牌、禁止标识、指示标志等） |

---

## 🏁 项目特色

- ✅ **小目标优化** — 针对交通场景中小尺寸标志专门训练，检测精度高
- ✅ **中文标识展示** — 检测结果以中文标志名称呈现
- ✅ **轻量级部署** — 支持 GPU 加速，也可在 CPU 上运行，适配本地与移动端
- ✅ **YOLOv12 前沿模型** — 采用最新 YOLO 架构，兼顾速度与精度
- ✅ **Django 全栈架构** — 前后端一体，开箱即用

---

## 📸 运行截图

| 网页端 | 移动端 |
|--------|--------|
| ![网页端](网页端演示.png) | ![移动端](移动端演示.jpg) |

---

## 🔗 相关资源

- **TT100K 数据集**：[Tsinghua-Tencent 100K](https://cgshhb.github.io/TT100K/)
- **YOLOv12**： [Ultralytics YOLOv12](https://github.com/ultralytics/ultralytics)

---

## 📮 联系作者

- **作者**：方泽铠
- **邮箱**：fangzekai117@gmail.com

> 本项目可用于教学演示、科研实验或智能交通产品原型开发。

---

## 📄 开源协议

MIT License
