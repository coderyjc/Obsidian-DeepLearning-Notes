## VTAB(19 tasks)

**VTAB (Visual Task Adaptation Benchmark)** 是一个由Google AI Research提出的视觉任务基准，旨在评估模型在不同任务上的泛化能力。VTAB包含19个视觉任务，涵盖了多种任务类型和领域。以下是VTAB的详细信息：

### 任务分类

VTAB 中的任务分为三大类，每类下有多个具体任务：

1. **自然图像任务** (Natural):
    - CIFAR-100: 100个类别，每个类别500张训练图像和100张测试图像，图像大小32x32。
    - Caltech-101: 101个类别，大约8700张图像，图像大小不固定，常调整为224x224。
    - Oxford-IIIT Pets: 37个宠物品种，大约7400张图像，图像大小不固定，常调整为224x224。
    - Oxford Flowers-102: 102种花卉，大约8200张图像，图像大小不固定，常调整为224x224。
    - SVHN: 街景门牌号码识别，共有10个类别，图像大小32x32。
    - Sun397: 397种场景，大约108000张图像，图像大小不固定，常调整为224x224.
    - DTD (Describable Textures): 47个纹理类别，大约5640张图像，图像大小不固定，常调整为224x224。
    - RESISC45: 45种遥感图像场景，每个类别2100张图像，图像大小不固定，常调整为224x224。
    - EuroSAT: 10种遥感图像类别，大约27000张图像，图像大小64x64。
    - Retinopathy: 5个糖尿病视网膜病变等级，35126张图像，图像大小不固定，常调整为512x512。
2. **特定领域任务** (Specialized):
    - Patch Camelyon (PCam): 癌症检测任务，图像大小96x96，包含327680张图像。
    - DeepWeeds: 9种杂草类别，17509张图像，图像大小不固定，常调整为256x256。
    - iNaturalist (Inat): 1010个自然物种类别，437513张图像，图像大小不固定，常调整为224x224。
    - ResNet50: 合成图像分类任务，10个类别，50000张图像，图像大小32x32。
    - SmallNORB: 立体图像识别任务，包含50个物体，每个物体5个类别，48600张图像，图像大小96x96。
3. **结构化任务** (Structured):
    - CLEVR/Count: 合成图像计数任务，大约70000张图像，图像大小320x240。
    - CLEVR/Dist: 合成图像距离比较任务，大约70000张图像，图像大小320x240。
    - dSprites/Location: 形状位置识别任务，大约737280张图像，图像大小64x64。
    - dSprites/Orientation: 形状方向识别任务，大约737280张图像，图像大小64x64。

### 标签与用途

- **标签**：每个任务的数据集都有具体的标签用于分类、检测、或分割等任务。
- **用途**：VTAB主要用于评估模型在各种任务上的泛化能力，测试模型在不同领域的适应性，适用于研究迁移学习、多任务学习和自监督学习等领域。

### 图像大小与类别

- 每个任务的数据集图像大小和类别数有所不同，具体信息如上所述。大多数图像会在预处理阶段调整为标准尺寸，如224x224或32x32等，以适应不同的模型架构和需求。

## ImageNet

**ImageNet** 是一个广泛使用的计算机视觉数据集，用于图像分类和物体识别任务。其详细信息如下：

**图像大小：**原始图像的分辨率不固定，通常在256x256到1024x1024之间。常用于训练的版本通常会调整到224x224或其他标准尺寸。

**类别：**数据集中包含1000个类别，涵盖了各种动植物、日常物品、工具、建筑等

**样本数量：**

- 训练集包含约128万张图像。
- 验证集包含5万张图像，每个类别50张。
- 测试集数量也约为10万张图像，但具体数量可能有所变化。

**标签：**每张图像被标注为一个或多个类别，并且提供了详细的类别层次结构。

**用途：**广泛用于训练和评估图像分类算法，是深度学习和计算机视觉领域的基准数据集。

## ImageNet ReaL

**ImageNetReaL** 是对ImageNet数据集进行重新标注的版本，目的是提供更准确和详细的标签。其详细信息如下：



**图像大小**：图像大小与ImageNet相同，通常在224x224或其他标准尺寸。

**类别**：保留了ImageNet的1000个类别。

**样本数量**：重新标注了ImageNet验证集中5万张图像。

**标签**：

- 每张图像提供多个标签（多标签标注），更准确地反映图像中的内容。
- 提供的标签通过众包方式获得，以确保高准确性。

**用途**：主要用于评估图像分类模型的性能，特别是针对ImageNet数据集进行训练的模型。

## CIFAR-10

**CIFAR-10** 是一个常用的图像分类数据集，由加拿大多伦多大学的Alex Krizhevsky和Geoffrey Hinton创建。其详细信息如下：

**图像大小**：每张图像的分辨率为32x32像素，RGB三通道。

**类别**：数据集包含10个类别，分别是：飞机（airplane）、汽车（automobile）、鸟（bird）、猫（cat）、鹿（deer）、狗（dog）、青蛙（frog）、马（horse）、船（ship）、卡车（truck）。

**样本数量**：

- 训练集包含50000张图像。
- 测试集包含10000张图像。
- 每个类别在训练集和测试集中分别有5000和1000张图像。

**标签**：每张图像被标注为一个类别。

**用途**：广泛用于图像分类算法的训练和测试，尤其是在深度学习模型的研究中。

## CIFAR-100

**CIFAR-100** 是CIFAR-10的扩展版本，包含更多的类别和更细粒度的分类。其详细信息如下：

**图像大小**：每张图像的分辨率为32x32像素，RGB三通道。

**类别**：数据集包含100个类别，类别分为20个超类，每个超类下包含5个子类。例如，超类“哺乳动物”下有熊、豹、狮子、猴子、浣熊等子类。

**样本数量**：

- 训练集包含50000张图像。
- 测试集包含10000张图像。
- 每个类别在训练集和测试集中分别有500和100张图像。

**标签**：每张图像有两个标签，一个是子类标签（细粒度分类），一个是超类标签（粗粒度分类）。

**用途**：主要用于细粒度图像分类算法的研究和测试，可以帮助研究者探索模型在处理更复杂的类别结构时的表现。

## Oxford-IIIT Pets

**Oxford-IIIT Pets** 是一个由牛津大学视觉几何组创建的宠物图像数据集，主要用于图像分类和物体检测任务。其详细信息如下：

**图像大小**：图像的分辨率不固定，通常在几百到上千像素不等。常用于训练时会调整到标准尺寸，如224x224或其他。

**类别**：数据集包含37个类别，包括25种猫和12种狗，每个品种作为一个类别。

**样本数量**：

- 总共包含7390张图像。
- 每个类别大约有200张图像，样本数量相对均衡。

**标签**：每张图像有类别标签，此外还提供了物体的边界框和分割掩码，以用于检测和分割任务。

**用途**：广泛用于图像分类、物体检测和图像分割任务，特别是针对宠物的相关研究。

## Oxford Flowers-102

**Oxford Flowers-102** 是一个由牛津大学视觉几何组创建的花卉图像数据集，主要用于图像分类任务。其详细信息如下：

**图像大小**：图像的分辨率不固定，通常在几百到上千像素不等。常用于训练时会调整到标准尺寸，如224x224或其他。

**类别**：数据集包含102个不同的花卉类别，每个类别对应一种特定的花卉。

**样本数量**：

- 总共包含8189张图像。
- 每个类别的样本数量不均衡，大约在40到258张图像之间。

**标签**：每张图像有类别标签，并且还提供了每个类别的图像数量分布。

**用途**：主要用于图像分类任务，特别是用于花卉识别和分类的相关研究。

这两个数据集都在计算机视觉领域具有重要地位，特别是用于训练和评估分类、检测和分割模型。