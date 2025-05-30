# CUDA开发环境安装

### 第一步: 安装 NVIDIA Studio 显卡驱动:

    
NVIDIA Studio 官方驱动 下载地址:

https://www.nvidia.com/en-us/drivers/

![img_3.png](img/img_3.png)
### 这里选择对应的显卡型号和系统
![img_4.png](img/img_4.png)
### 选择Studio Drivers 驱动下载和安装

### 2:查看显卡的驱动信息 

打开CMD执行:
```cmd
nvidia-smi  
```

![img.png](img/img.png)

可以看到为 CUDA Version: 12.9 ,表示当前显卡支持的cuda版本


第二步: 安装CUDA开发环境:
--------------
### 1:下载CUDA Toolkit
CUDA Toolkit 官方下载地址 :

https://developer.nvidia.com/cuda-downloads

下载必须登录账号,没有就注册一个

选择对应的cuda版本下载,这里要选择你显卡支持的版本

### 2:把下载的文件解压出来

得到3个目录 bin, include, lib

![img_1.png](img/img_1.png)

把这3个目录复制到cuda的安装目录

比如: C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v12.9

### 3:最后测试CUDA是否配置成功

打开CMD执行:
```CMD
nvcc -V
```
![img_2.png](img/img_2.png)

### 安装成功

### **附: PyTorch 安装**
```bash
# 基础安装（CPU版）
pip install torch torchvision

# GPU版（需CUDA环境）
pip install torch torchvision --index-url https://download.pytorch.org/whl/cu118
```
- 验证 GPU 是否可用：
```python
import torch
print(torch.cuda.is_available())  # 输出 True 表示GPU可用
```



