## 直接torch print这个net

自带的，但是不完整，没有层与层之间的关系。

```python
print(net)
```

## torchsummary

```bash
pip install torchsummary
```

net需要在gpu上，第二个参数是大小的元组（C，H，W），第三个是batch_size

```python

from torchsummary import summary

summary(net.to(device=try_gpu()), (1, 28, 28))
```

## torchview + graphviz

### 安装graphviz

1. 下载Graphviz

直接在官网下载安装即可 https://graphviz.org/download/

需要下载安装包解压之后需要把bin目录添加到环境变量，还要把dot.exe添加到环境变量

如果user环境变量添加之后找不到dot文件，则添加到system环境变量中。

2. 安装graphviz包

```bash
pip install graphviz
```

### 安装torchview

```bash
pip install torchview
```

```python
from torchview import draw_graph  

model_graph = draw_graph(model, input_size=x.shape, expand_nested=True, save_graph=True, filename="torchview", directory=".")  

model_graph.visual_graph
```

