# 制作更高更妙的MC地形 WorldMachine基础教程

### 本文档使用 CC BY-NC-SA 3.0 CN 协议（https://creativecommons.org/licenses/by-nc-sa/3.0/cn/legalcode） 共享。除必须引用的部分，其权利属于各自所有人。

### **您可以自由地：**

共享——在任何媒介以任何形式复制、发行本作品。

演绎——修改、转换或以本作品为基础进行创作。

### **惟须遵守下列条件： ** 

**署名** 您必须给出适当的署名，提供指向本许可协议的链接，同时标明是否（对原始作品）作了修改。您可以用任何合理的方式来署名，但是不得以任何方式暗示许可人为您或您的使用背书。

**非商业性使用** 您不得将本作品用于商业目的。

**相同方式分享** 如果您再混合、转换或者基于本作品进行创作，您必须基于与原先许可协议相同的许可协议 分发您贡献的作品。

**不得增加额外限制** 您不得适用法律术语或者技术措施从而限制其他人做许可协议允许的事情。


 本概述文本仅仅强调部分核心特征和真正许可协议的部分条款，不是正式许可协议。您应当在使用授权作品前，仔细审阅真正许可协议的所有条款。

------

**以下部分是教程正文。**

------

![](https://thingy.top/view.php/7973824b14531975643cb68ecbd76cbb.png)

# **第零章 我是 WM World Machine你学会了吗**

## **#0-0 序言**

赤道几内亚承运，介介子诏曰：

这篇教程完全针对Worldmachine+Worldpainter流程的Minecraft地形制作，且内容十分基础，适合已经学习Worldpainter，希望制作出更加真实的地形的地形师阅读。在阅读本教程前，你需要有基本的计算机常识。地理知识并不是必备的，但了解自然地理基础知识有助于地形的制作。学习本教程后建议通过学习他人工程进阶，而非继续依赖各类教程。

地形和其他领域不同的是，地形几乎不能脱离圈子闭门造车。你需要放平心态，与地形圈的其他人交流，因此，你务必需要了解提问的智慧、懂得如何与其他人相处。双标和伸手等行为解决不了任何问题，还会让你成为一个乐子。

地形圈的历史相当悠久，本贴给出的译名均是地形圈的长久的发展历程中形成的说法，那些很少用翻译的专业名词均没有给出译名，目的是便于读者在地形圈的交流，以免造成沟通困难。本文的一些描述可能极为不准确甚至错误，目的是便于理解，很多情况下我们并不需要过于准确的语言，毕竟我们针对的是Minecraft地形制作。

至于我为什么要写这篇教程，虽然地形圈一贯反对伸手的行为，但是这并不妨碍人是懒狗的本性。虽然已经有很多人做过了Worldmachine的教程，但多数为视频教程，只有少数图文教程几乎还全部弃坑。我作为一条资深懒狗，进行一个烂的摆，在入坑很久之后一直是纯WP地形，后来才逐渐开始使用WM。然而WP的局限性还是很高的，很难做出极为真实的效果，因此如果你想入坑地形，WM的学习是必需的。我相信一定有和我一样的懒狗，因此写了这篇懒狗教程。这篇教程不是很长，字数统计显示仅需要30分钟就能读完，但边读边打开WM试试才能真正理解。

## **#0-1 下载与安装**

World Machine是一款功能强大的地形建模软件，官网地址<https://www.world-machine.com/>。目前售价为社区版免费、独立开发者199美元、专业版299美元、工作室版1999美元。社区版限制较高，不推荐使用，本文不提供直接的破解版下载地址。您可以前往画忆妙妙屋等网站自行搜索。另外也推荐使用花开汉化的版本，群号为854909057。本贴使用版本为v4031 Professional 英文原版。为了保证顺利的理解本文，推荐安装v4031。安装后，如果遇到启动失败相关问题，可参考花开的WM启动问题处理文档（见本文附录）。

## **#0-2 操作逻辑**

WM的操作逻辑是节点操作，一般地形制作流程为形体－调整－自然化－上色。这里仅做一个简单介绍，WM流程在第一章会重点教授。一般称WM的节点为模块。WM的模块效果各异，但基本构造相同。

以图中模块为例，左侧为输入端，右侧为输出端，上方为数据接口（4027版本开始不再主动显示），下方为遮罩接口。简单来说，左侧接入的内容经过模块的处理后传给右方，这就是模块的工作原理。

需要注意的是，模块名称左侧还会亮起指示灯，青绿色表示正常工作，黄绿色表示尚未构建，蓝色表示已构建但内容已被删除，红色表示接入方法有误，红叉表示WM工作异常。

![](https://thingy.top/view.php/fcb265ff3b5ef00c370bd98a1d529204.png)

## **#0-3 基本操作**

开始之前，先简单将WM界面分个区，方便介绍。

![](https://thingy.top/view.php/e77227686b59d607684091f0d5cbded3.png)

模块栏：取模块的地方，没什么好说的。

预览区：大框里面显示的是当前模块预览效果，你可以修改下面的选项来调整光照，水体，描图等等效果。

模块陈列区：会显示出来你摆下的每一个模块。历史栏里可以保存你的操作记录。

工具栏：其实每一个有图标的选项都是文字选项卡里面比较重要的选项，这里只重点说一下下面那行有图标的。从左到右依次是新建工程、打开工程、打开示例工程（强烈推荐翻阅，有助于快速上手）、保存、导出页面、工程设置页面、WM设置页面、随机种子、显示/隐藏侧栏、修改工作布局、工作页面、布局界面、探索页面、3D预览、2D预览、构建全部模块、构建当前模块、分块构建。

至于右键模块弹出的窗口，这里直接借用花开汉化版的翻译，相关快捷键也有体现，不再赘述。

![未标题-1](https://thingy.top/view.php/70c3a0b444bc5ce32fe85573c8fe27f6.png)

## **#0-4 尺寸对应**

地形圈普遍认为，Minecraft地形到WorldMachine地图的比例一般是1个方格的长度（Minecraft中的1米）相当于WM中的10m的长度。根据该规则，应将工程设置页面中的子选项卡Scene Setup中Width（或Breath）的值与Resolution的值设置为 x km 与 100x 。1k地形即指10.24km x 10.24km的地形，其他尺寸同理。例如Width为10.24km，Breadth为10.24km，Resolution为1024x1024。这就是所说的1k地形。如果需要非正方形尺寸地形，只需要修改Square Aspect为Any Aspect Ratio。如果您的尺寸设置正确，Detail scale的值应为10.00m/pixel。WM默认的地形高度为4km（400方块），需要将Project Setup选项卡中Dimension Preference的值根据需要修改为2.56km（256方块）或3.84km（384方块）等等。

![](https://thingy.top/view.php/e1b2f048e163172c7de1c179f19ca589.png)

# 第一章 **年轻人的第一个WM工程**

## **#1-1 创建形体**

这里以制作一个2k山区为例，为大家介绍具体的WM地形制作流程。首先根据#0-4中所教，创建一个2k世界。

随后，我们可以在模块栏中Generator一栏，选择Advanced Perlin（高级柏林噪声）![](https://thingy.top/view.php/c3c9aebb26862c12a1866c8f47ce073a.png)，这是一个十分常用的模块。

我们就可以得到这样的形状，称之为噪波，这是多数地形的开始。

![](https://thingy.top/view.php/550a0dc4020804bf73a9720e63ecd267.png)

我们需要对其进行一些参数调整，双击模块，将Scale的值调到20km，适当修改Steepness和Middle elevation的值，得到这样的形状。大家不妨自行尝试，调整各个参数，以便了解参数对应的效果。

![](https://thingy.top/view.php/fbf97c6d68304667740e68095ba1ff8c.png)

## **#1-2 调整形状**

随后，拿出Filter栏中的Displacement![](https://thingy.top/view.php/405ceca14b97453d7d2fb30db82a4950.png)模块和Generator中的Basic Noise![](https://thingy.top/view.php/46072f39b97ff243db15935c8640d479.png)模块，以这种方式连接，对我们之前Advanced Perlin的地形进行一些扭曲。Displacement模块的Distance需要适当调整为1.5km左右，Direction视情况决定是否调整。

![](https://thingy.top/view.php/d2461f47e1e7faea2f6a98f63826b975.png)

![](https://thingy.top/view.php/ab5b73aef1647c735aaf2ecbae5ba49a.png)

## **#1-3-1 自然化处理：侵蚀**

再到Natural栏中找到Erosion（侵蚀）![](https://thingy.top/view.php/f16c3a9b1c4d24701e2ab6e5b41cf935.png)模块，连接到Displacement的后面。在右上角Presents栏中，选择Deeply Carved预设。WM自带的许多预设都十分好用。

![](https://thingy.top/view.php/941ee351fe30f5c69e9a4574c449fa4d.png) 

## **#1-? 随机应变**

我们终于获得了一个像山的形状，但这还不够，我们注意到一些地方由于侵蚀的效果，已经碰到了地形的底部。我们只需要再摆下一个Advanced Perlin模块，并找到Combiner中的Combiner![](https://thingy.top/view.php/6375e94e4ccb07b1ec82d5803ff20361.png)模块。将Advanced Perlin中的预设选择为Swiss Cheese，适当拉低Middle elevation的值，然后将Combiner的模式修改为Screen（防止地形顶破限高)，并将强度拉到1，并以这样的方式连接模块。可以看到地形碰底的问题已经得到解决。

![](https://thingy.top/view.php/0aa24cbcc0b6783922ee37e98d10be35.png)

![](https://thingy.top/view.php/7fdf8625b686533722ca5148ed845751.png)

## **#1-3-2 自然化处理：风化**

我们再到Natural栏中找到Thermal Weathering（热力风化）![](https://thingy.top/view.php/3955726ae2d322d3e13ce6a323c5bd1d.png)模块，直接接入即可。但是我们好像很难发现地形有了什么变化，不妨试着打开3D预览页面中的比较线![](https://thingy.top/view.php/1ee2dde29f8cc9a733d28dd64d78d0b1.png)，这样我们就可以直观看出地形前后差距了。可以发现，风化过后的地形，高坡度地区产生了一些碎石。

1![](https://thingy.top/view.php/a5657a3185c2305a64595a1ec272fe14.png)

## **#1-4 上色**

上色较为复杂，这里我们使用上色宏解决。找到工具栏中Macros（宏）一栏，找到Texturing中的Quick Texture摆下，接入后我们就可以快速得到地形上色。宏的本质是多个模块整合到一起，制作方法后续章节再讲。我们再找出View模块栏中的Overlay Preview![](https://thingy.top/view.php/e7c25e62cef2914915d1aa70da9f28cb.png)，上口接入地形，下口接入上色，预览效果。

![](https://thingy.top/view.php/e62b875489d99d4de2962f27828fa47a.png)

## **#1-5 导出**

我们的地形已经制作完成了。接下来找出Output栏中的，Height Output![](https://thingy.top/view.php/ffa2d4956b1681201d0205a1181f1d58.png)和Bitmap Output<img src="https://thingy.top/view.php/ec0e4e06ba14fecbbb80b09e6c7c2def.png" style="zoom:120%;" />，分别将地形和上色接进去，修改文件名。然后打开导出页面![](https://thingy.top/view.php/03c86c732ccc97f3c2f0ee4d0fe8e1b7.png)，选择Export All，我们就可以在显示的目录中找到保存好的两张图片。

![](https://thingy.top/view.php/23b4e28fa32897fe4aeb653e0bc2aa53.png)

# 第二章 **模块效果**

我们已经知道，做地形需要依靠模块的堆砌，那么为了做出更好的地形，我们有必要了解一下常用模块的效果。

## **#2-1 自然化**

自然化其实并不摆在模块栏的前列，但自然化效果对地形制作十分重要，因此我们第一个先讲自然化。

### **#2-1-1 自然化：侵蚀（Erosion）**

侵蚀是新手时期最重要的自然化模块。侵蚀的效果还是很显而易见的，可以看到我们的地形上出现了很明显的沟壑。

![](https://thingy.top/view.php/b6428d7e6d90f1c97884b740ac1e4ce3.png)

接下来简单介绍一下比较重要的参数。也许描述不是特别十分非常严谨，但是应该可能大概估计是足够新手使用了。

Duration（侵蚀时间）：数值越大效果越强。

Rock Hardness（岩石硬度）：数越大沟越深。

Sediment Carry Amount（泥沙量）：数越大沉积越重。

Geological-time Enhancement（冰川侵蚀/地质时间增强）：打开后会增强侵蚀效果。如果关闭，多数情况下侵蚀模块对地形主体以外的地方产生作用的现象将会消失。

侵蚀模块有三个入口，第三个没啥用。

Hardness Mask：接入灰度图的值会乘上参数中的Rock Hardness，乘积来确定岩石的硬度。

侵蚀模块有四个出口，相信聪明的你大概看一下就懂了。Flow、Wear一般不译，Deposition一般称作沉积。

当然，作为一个地形圈资深养老人，我十分建议大家去试试WM给的参数，不必自己一个一个去调，在参数的基础上作出一点修改即可。比如Deeply Carved预设，我们适当拉低一些岩石硬度，直接就有硬山了。

![](https://thingy.top/view.php/e179349000577ba66588ac61d9c69f38.png)

### **#2-1-2 自然化：风化（Thermal Weathering）**

当你继续深入学习地形之后，你就会觉得——

侵蚀你就是歌姬吧，你来风化大街，指定没你好果汁吃嗷

![](https://thingy.top/view.php/8a69de679798477208e5b62d117e3bce.png)

Talus Production（碎石量）&Intensity（强度）：控制产生碎石的多少

Talus Repose Angle（碎石坡度）：如果坡度大于这个值，地形就会产生滑坡，在山脚形成碎石。

Fracture Size：屁用没有。只有在数值差异极端巨大的时候能观察到些许差异。他就跟语文老师讲的那个勾八课外文言文一样，出个死勾八难的实词结果这玩意是你这辈子最后一次见到，高考从来就没考过。

Talus Size（碎石尺寸）：数越大堆积坡越凹凸不平。

Simulation Length（碎石距离）：数越大碎石就滚得越远。

特别需要注意的是，这个模块他的旧版本也特别特别特别好用，这里不过多叙述，只提供给大家两张效果图和对应参数，读者自证不难。

![](https://thingy.top/view.php/d4b7a41aed36c51a58d05d1d6e4d8576.png)

![](https://thingy.top/view.php/5c1962a761757085296d4c6a415dfe29.png)

![](https://thingy.top/view.php/55d50aa038e62920581ba6c9de66b1c3.png)

![](https://thingy.top/view.php/1ccf481a91e8fd64d13e64575d2f3c41.png)

### **#2-1-3 自然化：地层（Strata）**

![](https://thingy.top/view.php/0cdba41acaf6a65d2214253ea38fddab.png)

你把它理解成阶梯化Pro Max就行，虽然我们还没接触阶梯化（

Strength（强度）：字面意思。

Scale（范围）：数值越小分层越多。

Smoothness（模糊程度）：字面意思。

Layer（层化程度）：字面意思。

Tint（角度）：控制纹理的角度，因为容易和下一个参数弄混，所以干脆放图解释。

![](https://thingy.top/view.php/f1334f787e1ccf2552dcd8b989aa7851.png)

![](https://thingy.top/view.php/519eeec5e6feb245138c0b3c5b7b1089.png)

Heading（方向）：控制纹理倾斜方向，放图。

![](https://thingy.top/view.php/941d6cfd79b1d8f210af40847a691cbf.png)

![](https://thingy.top/view.php/26662b9109489d22e87d6959180a788a.png)

### **#2-1-4 自然化：雪（Snow）**

![](https://thingy.top/view.php/9fe0d833e61758810af596b7e10468bc.png)

Snowfall（降雪量）：值越大，雪对地形的平滑程度越高。

Stickiness（黏度）：值越大，雪的黏性越强，更容易黏在坡度高的地方。

Snowmelt Mask Input（融雪遮罩输入）：值越大，第三个输入端口接入的遮罩的范围内的雪融化越多。

这一模块可搭配Natural Effects类中的Snowmelt宏使用，辅助进行融雪。

### **#2-1-5 自然化：海岸侵蚀（Coast Erosion）**

这铸币模块属于是特别有用的，而且不可替代，但是实在是太铸币了，在WM的某次逆天改版之后，给的Water不是很精确，导致做水流的时候一堆破事。

![](https://thingy.top/view.php/e46410172e8f72bed8b4a207bf1898d2.png)

Sea Level（海面高度）：字面意思。点那个按钮可以自己对应场景设置的海平面高度。

Beach Size（海滩大小）：字面意思。海岸会从基础线开始向海里拓展。

Inland Height Influence（陆地影响程度）：和上面的海岸大小相反，修改这个参数，海岸会从基础线开始向陆地拓展。

Underwater Smoothing（水下平滑程度）：字面意思。

### **#2-1-6 自然化：Create Water**

这里只介绍参数，河流制作在后续会系统讲解。参数直接引用我进阶视频教程中的，懒狗了属于是。

![](https://thingy.top/view.php/e8990d654b9f53f1c04a7fb7a325349e.png)

![](https://thingy.top/view.php/ba4fc3f2d0af3598238629e47baf0e93.png)

## **#2-2 生成器**

**生成器是绝大多数地形的开始，也是许多流程中不可或缺的。**

### **#2-2-1 生成器：高级柏林噪波（Advanced Perlin）**

![](https://thingy.top/view.php/0e389779fcb3f899161015a9bc34e7dc.png)

接口方面，也就形状、扭曲、精度三个指导接口，挺简单的，指导强度在参数里面隐藏起来了，勾选上显示更多参数就显示了。参数简单介绍几个，因为我懒，直接贴一个3026 版本的模块界面汉化图。

Feature Scale：噪波规模。越小纹理越密集，地形凹凸起伏越多。

Style：噪波样式。

Persistence：叠加精度，越低噪波越圆润。

Lacunarity：叠加规模，也就是又叠上来的小噪波的Feature Scale。

Octaves：叠加数量，越高噪波越复杂。

Seed：随机种子。

Steepness：噪波起伏。

Middle Elevation：中位高度。

![](https://thingy.top/view.php/1ab67252db4d258340f441ac7d4da447.png)

![](https://thingy.top/view.php/610592e654ea6a3fd12589af3aee78ef.png)

### **#2-2-2 生成器：基础噪波（Basic Noise）**

和Adv Perlin大同小异，Style有点差别，不再赘述。

![](https://thingy.top/view.php/1045ba0dc873e0cc6dbd5e72462a3e94.png)

### **#2-2-3 生成器：Color**

颜色生成器是生成纯色的简单模块。默认情况下，创建一个全图范围的单色。但是，通过使用遮罩输入或将输出与选择遮罩组合，颜色生成器将成为上色工作的基础。

### **#2-2-4 生成器：Constant**

常量生成器仅创建指定高度的水平平坦地形。

### **#2-2-5 生成器：File Input**

从外部导入地形的模块，应该没有什么好说的，调Type可以修改导入文件的类型，Width调长宽，一般来说知道这点就够了，也许你足够牛逼的时候还会接触到重采样方式，其他估计是永远用不到，但是3026版汉化依旧汉化了每一个选项，有需要可以看看。

![](https://thingy.top/view.php/c8187e32590f8b2a3b7bc45f53a05d81.png)

![](https://thingy.top/view.php/ea468680a678d46e6b1fdf8474c6297f.png)

### **#2-2-6 生成器：Gradient**

生成斜面用的模块。没什么好说的。Tilling里面四种模式，分别是硬边缘和软边缘的单个斜面，以及单面和镜像的多个斜面。

![](https://thingy.top/view.php/b67777ee46af88d9a80fb6b974d4071c.png)

### **#2-2-7 生成器：Radial Grad**

Radial Grad能创建一个简单的以空间中的一个点为中心的几何形状。

![](https://thingy.top/view.php/d03fc8f6924f9a0563622e1083c807a2.png)

这里我直接翻译了官方文档，然后补上一点官方文档没有的。

Radius（半径）：形状应覆盖多大的面积。默认值为8km，恰好完全填充了默认的地形范围。

Type（类型）：

球形Spherical：在边缘急剧下降的圆形轮廓。

高斯Gaussian：呈高斯分布的丘形轮廓。

钻石Diamond：看起来很像金字塔的不断倾斜的轮廓。

正方形Square：方形轮廓。它保持水平，直到边缘急剧下降到零为止。

锥形Cone：在所有方向上恒定向下倾斜到零。

指数Exponential：临近中心处下降快而边缘处下降慢，类似幂函数。

正弦Sinusoidal：在侧面看起来和正弦函数图像一样的形状。

圆锥横扫Conic Sweep：照着GAEA学的一个形状，长这个样子。

![](https://thingy.top/view.php/d8e2153bd93293b00219217ffc7e5ac4.png)

### **#2-2-8 生成器：Voronoi**

有些类似水波纹，十分重要的模块。

![](https://thingy.top/view.php/2dd68c0ad5d010643318630cb86470a4.png)

Feature Scale：规模。

Style：类型。这个模块的类型很多，可以自行尝试，需要注意的是他有几个生成类似麦田轮廓的细胞模式。

![](https://thingy.top/view.php/06e99dca2bf1c1c9dc2f5006168891e0.png)

Crystallize：打开之后模块只接受彩图，对彩图执行晶格化操作。

### **#2-2-9 生成器：Shapes**

十分重要的模块，做综合地形必不可少，旧版本名为Layout Generator。

双击之后，我们就会发现这个模块不会弹出参数窗口，而是直接跳进了布局页面。

![](https://thingy.top/view.php/774bc8e924326d922e59203f13e90926.png)

左侧是画形状的地方，右侧是参数。

Quality：决定预览质量的，和实际效果没有关系，你build完之后都一样，看你设备性能自行决定。

Background Value：地板的高度值。

Invert Output：反向。

Breakup Shapes：勾选上后形状会随机分形。弹出来三个选项分别决定强度、范围、粗糙度。这一强度是指趋向分形后地形的强度。

Add Shapes：选择形状。需要注意的是多边形和线在画的时候可以单点也可以拖拽，画完双击右键即可。画完之后也可以对锚点再次进行调整。

Enabled：决定形状是否生效。

Default Value：形状最大高度。

Opacity：不透明度。

Type：Union模式在任意点都使用最高的形状，Subtract雕刻现有的地形。

Distance：过渡距离。

Type：类型。一般情况下，一定一定一定要改成Linear，

Direction：决定向外过渡还是向内过渡。

Shape Breakup：分形强度。这一强度是指真正的分形强度。

## **#2-3 滤镜**

### **#2-3-1 滤镜：Add Noise**

噪化地形。

![](https://thingy.top/view.php/21d4818d2af97e153f5d7f8f28726fbd.png)

### **#2-3-2 滤镜：环境光遮蔽（Ambient Occlusion）**

在3028时代有个大神想要AO效果，于是用了360个角度的光照图叠出来了AO，官方看见之后连声叫好，正义制作了AO模块，只留下暴力大神在风中凌乱。

![](https://thingy.top/view.php/3f6965973acf0dbc92afb764b30fc225.png)

我之前录过一期视频教程（https://www.bilibili.com/video/BV19o4y1D7rF）专门讲这个模块的，有需要可以看看。

### **#2-3-3 滤镜：Bias/Gain**

地形圈有这么一句玩笑话，如果你想让你的地形看起来高端，就把Clamp换成Bias/Gain。这个模块的效果和Clamp的Rescale和Expand模式几乎一致，但是相对用的人少。用法和PS的亮度/对比度相同。

### **#2-3-4 滤镜：Blur**

模糊，除了一般的高斯模糊，这个模块还提供了径向模糊，修改Method的选项即可。

![](https://thingy.top/view.php/4db03aca0542445ae9716d648a7f71b1.png)

![](https://thingy.top/view.php/64ee4813dad164b448c130abc9111044.png)

### **#2-3-5 滤镜：Clamp**

十分重要的一个模块，可以压低/削顶/抬高地形，分别对应Operation的三个选项。

这个模块还提供了一个Find Extent的按钮，点击这个按钮，WM就会将Clamp的模式转为Expand，并自动帮你对应到地形的最低点和最高点，让地形占据整个高度范围。

### **#2-3-6 滤镜：晶格化（Crystallize）**

可以将地形转化为六边形或正方形的堆叠。4027新增的模块，还没有模块图标。

![](https://thingy.top/view.php/f00fa39e411fc9a4d6e26e2b06cc46a1.png)

### **#2-3-7 滤镜：曲线（Curve）**

和你在PS里面用的曲线一样的，没什么可说的。对于新人十分难以控制，不推荐。

![](https://thingy.top/view.php/e888bdcf78c74279b27d6920852ca416.png)

### **#2-3-8 滤镜：Displacement**

特别特别重要的一个模块，可以对图像进行位移操作，或者俗称是扭一扭。第二个接口必须接东西，Vector模式下第三个接口也必须接东西。而且你会发现，伴随着Type的变化，端口的名字也会发生变化。

![](https://thingy.top/view.php/b754a0113e1aa6621fc54ba42c929c43.png)

Type：

Angle And Distance，你可以简单理解为，把第一个端口的地形往第二个端口的形状去扭，第三个端口做引导，有没有都无所谓。

Vector模式下，第二个接口控制X怎么扭，第三个接口控制Y怎么扭。

这样的说法及其不正确，只是为了方便理解。

Direction：控制位移的方向。

Distance：控制位移的距离。

### **#2-3-9 滤镜：Equalizer**

屁用没有。

但是有点屁用，在一些遮罩，比如Snow的Snow Mask遮罩里面，一些地方及其不突出导致你预览起来和到WP里面刷的雪是两回事，这时候只要接入Equalizer，就能让原本不明显的地方突出起来，以便我们进行下一步过滤。

![](https://thingy.top/view.php/a0fb69d2b04d21718845d67678736777.png)

### **#2-3-10 滤镜：水流重构/河道预处理（Flow Restructure）**

字面意思，能有效解决Create Water的断流问题，水系问题后面会系统地讲，目前你只需要知道，这个模块可以来开一些大型的河道，让地形的高低落差能够实现水流畅通而不是堵成湖泊。

### **#2-3-11 滤镜：Expander**

对地形进行扩张，处理遮罩和造山的利器。

![](https://thingy.top/view.php/cbddceee20b57d41ce7cc26312d54d94.png)

Action：扩张方式，Expand向外扩张，Shrink向内收缩，Open和Close夹在两者之间，Close更靠近Expand，Open更靠近Shrink。

Type：扩张种类，分别是高斯（类似圆形）、线性坡度（类似棱锥）和方块。

Distance：扩张程度。

这个模块还有一个旧版本，WM2.x有Circle模式的扩张，十分好用。

![](https://thingy.top/view.php/ca2bf6bb2a373708b345834a9173649b.png)

### **#2-3-12 滤镜：Flipper**

翻转。有时候你好不容易画出来好看的大陆架，但是发现方向错了，一正过来不那么好看了，就可以翻转一下。不太常用。

### **#2-3-13 滤镜：Inverter**

反相。

### **#2-3-14 滤镜：概率（Probability）**

![](https://thingy.top/view.php/9f570c99d3468b93a70353317811afea.png)

我做过这个模块官方文档的翻译，在这里直接引用了。

概率滤镜将输入图视为概率密度函数，并创建一个根据该密度函数随机散射单个像素点的输出蒙版。这对于物件放置以及上色十分有用。

Probability Type（概率类型）：使用哪种分布模型。目前只有一种选择—在地图上均匀分布像素点。

Bias（偏离）：偏离参数规定根据输入端数据随机创建白色像素的概率。调整此值将导致创建更多或更少数量的点。偏离值为0将不产生输出，偏离值为1将产生全白遮罩。默认值为0.5。

Strength（强度）：施加偏离后，该参数将进一步降低创建点的可能性。值为1.0无效，而值为0将确保不创建任何点。

结合以上内容，有几个例子：

偏离值为1且强度值为0.5时，所有位置生成点的机会相同（偏离1.0），但是强度为0.5时，意味着输出将是随机的白色噪声，而不是纯白色。

0.5的偏离值和1.0的强度值将创建一个最类似于输入值的贴图，只是单点绘制而不是连续绘制的。

### **#2-3-15 滤镜：Ramp**

取一个高度之后对这个高度以上的地形进行翻转，最终形成分层的图案。

![](https://thingy.top/view.php/a704d3b1c313e26394b16496ab44381f.png)

### **#2-3-16 滤镜：Simple Transform**

功能十分丰富的一个模块，可以实现各种简单的高度调整。效果强度由Intensity控制。

### **#2-3-17 滤镜：阶梯化（Terrace）**

![](https://thingy.top/view.php/968977eb5914d2c6ad52548a35e72053.png)

Terrace Method：控制阶梯化的形式。Simple不过渡，Shar锐利边缘，Smooth柔和边缘。

Number Of Terraces：阶梯化层数。

Terrace Shape：效果强度。越接近0.5越弱，且小于0.5向外凸起，大于0.5向内凿出。

Terrace Layering：在各阶梯间填加的小一点的阶梯的层数。

## **#2-4 合成器**

对两种地形进行合并的模块。

### **#2-4-1 Combiner**

一共有十四种合成方法。参数只有一个Strength，控制合成强度。由于合成方法众多且难以用文字叙述，这里只介绍几个最为常用的。

Average：求平均值，参数为0.5时两个输入的权重相同，越接近0第一个输入的权重越大，越接近1第二个输入的权重越大。

Add：加法。

Subtract：减法。

Multiply：乘法。

Screen：类似Add，但这个模块不会碰到高度上限，综合地形叠加地形常用。

(Smooth) Max：保留最大值。

(Smooth) Min：保留最小值。

### **#2-4-2 Multi Chooser**

将地形按照高度分为多个小块后，在对应高度使用对应接口的地形进行操作。可以实现阶梯化效果。

Number Of Inputs：输入接口和分层的数量。

Transition Contrast：可以简单理解为阶梯化程度，这样说并不准确。

图片中，我将接口数量设置为2，在第一个接口连接了高低落差很大的噪波，第二个接口接入平面，第三个接口接入Voronoi。可以看到高度高的地方变为了Voronoi，而高度低的地方变成了平面。

![](https://thingy.top/view.php/8da27a6a871efd613658f1a0e65927d6.png)

## **#2-5 选择器**

选择器可以帮助你选择出各种遮罩以便限定模块操作范围。模块颜色为紫色。

### **#2-5-1 选择器：光照角选择（Select Aspect）**

![](https://thingy.top/view.php/fcafb6022a83ecd1ca04b5f61ef739ae.png)

Heading：太阳方向。0对应北方，随着参数变大逆时针旋转。

Elevation：太阳高度。0对应水平，90对应垂直。

### **#2-5-2 选择器：Select Color**

选择颜色。

### **#2-5-3 选择器：Select Convexity**

选择凹凸。Strength参数控制遮罩的对比度。

### **#2-5-4 选择器：Select Height**

选择高度。通过Range来控制选择范围，Falloff控制过渡范围，选择Invert Selection可以反选（起到节省一个Inverter的作用）。

### **#2-5-5 选择器：Select Roughness**

选择粗糙度高的地方。

![](https://thingy.top/view.php/be08f6e637f4f77999a22dbaa1dd9138.png)

### **#2-5-6 选择器：Select Slope**

选择坡度。通过Range来控制选择范围，Falloff控制过渡范围，选择Invert Selection可以反选（起到节省一个Inverter的作用）。

### **#2-5-7 选择器：Select Wetness**

选择湿度。Moisture控制水汽浓度。

## **#2-6 预览器&导出器**

旧版本的WM里面这两种模块就在一起，加上制作MC地形需要的相关模块少，因此合在一起讲。两类模块都是红色。

### **#2-6-1 预览器：Overlay View**

将灰度图或彩图直接覆盖在地形上，参数控制覆盖程度。

### **#2-6-2 预览器：Scene View**

4027更新后功能极为丰富，可以预览地形、（PBR）材质、水系、法线、环境光遮蔽等的效果。

### **#2-6-3 导出器：Height Output**

导出灰度图用。

Filename：文件名以及文件路径。

File Format：文件格式。

Output File on every Build：是否在每次构建时都进行导出。

Participate in Tiled Builds：是否在进行分块导出时导出该文件。

Write to Disk：直接导出该图片。

### **#2-6-4 导出器：Bitmap Output**

导出彩图用。

Filename：文件名以及文件路径。

File Format：文件格式。

Output File on every Build：是否在每次构建时都进行导出。

Participate in Tiled Builds：是否在进行分块导出时导出该文件。

Write to Disk：直接导出该图片。

# **第三章 基本思路**

## **#3-1 利用遮罩**

利用遮罩是地形制作中一个至关重要的方法。

### **#3-1-1 使用遮罩**

首先我们当然需要知道的是，遮罩究竟是干什么的。如果你曾经接触过PS等图像处理软件，这个东西就很熟悉了，但不知道也没关系，遮罩的作用是限制模块的操作范围。

比如，我们只需要这样连接模块并合理调整模块参数，就可以限制阶梯化模块仅作用在地形较低处的洼地上。

![](https://thingy.top/view.php/ece1cb2bbe49e52e08d160c1e532bec1.png)

![](https://thingy.top/view.php/2b6dcd347fe58bab7e4ec2ff337d7bac.png)

### **#3-1-2 处理遮罩**

还是这个例子，但是我们这次想限制阶梯化在地形坡度高处，我们直接连接，会发现地形变得很噪。

![](https://thingy.top/view.php/b424e64584bc538eef484b18a19e84b1.png)

这种情况是因为我们使用的遮罩过于细碎了，如何解决呢，不妨尝试连接一个Blur模块，将强度改为20m，可以看到问题得到解决。

![](https://thingy.top/view.php/e987a01578ac31744604a2380a5f0ba8.png)

![](https://thingy.top/view.php/5ec388c95bad95f51bf65235fc5dee1a.png)

类似的，我们也可以通过Expander模块解决这个问题。

### **#3-1-3 合并遮罩**

当我们把上述两个方法的需求加起来，想操作坡度高且海拔低处呢？对于这个例子，我们可以让Select Height的结果作为Select Slope的遮罩，再用前面说的Blur模糊遮罩，即可实现这个效果。

![](https://thingy.top/view.php/c75bab13375b9421cb6d5b68a18ef456.png)

![](https://thingy.top/view.php/8f42d18a6a9b95033545c8523ccfd310.png)

但是这种方法，我们会遇到一个严重问题：不是所有遮罩都来自Select类紫色模块，比如侵蚀的Flow遮罩，我们总不能去给侵蚀接遮罩吧。这时候，我们可以尝试Combiner的Multiply模式，将参数拉到1。例如下图，仅操作Flow侵蚀流与低海拔区域的交集。

![](https://thingy.top/view.php/6d666b5296ddfc3860768b4ed8f3fc83.png)

![](https://thingy.top/view.php/ba578797c6e2f878245c20c6ffa56102.png)

类似的，根据我们对于合成各遮罩权重的需要，我们也可以选择Add和Subtract等模式，各模式差异读者自证不难。

### **#3-2 修改参数**

“多练。”

虽然前文已经介绍了大多数模块和常用参数，但光看和练习绝对是不一样的。我在第零章建议大家的一个方法仍然适用。调整参数的同时，看着左上角的小窗观察效果变化，有助于我们更好的了解参数对应作用。

但这样做也有弊端，WM的预览精度极低，可能参数变化并不能带来特别显著的效果变化，这里介绍另一种比较效果的方法。

对于一个模块，我们只需要在3D预览界面选择打开A/B比较线即可。但我们如果想要比较多个模块叠加起来后对地形的共同效果，则可以尝试使用Combiner的Average模式，参数拉到1，上口接原地形，下口接处理后地形，这样就能通过比较线看出差异了。

![](https://thingy.top/view.php/9f82a7b4e53b34552b8f40091c9870a6.png)

![](https://thingy.top/view.php/692ce477cf844caf22a40123e185f927.png)

类似的，如果我们纠结于两种效果的取舍，也可以通过该方法进行比较，选择更合理的效果。

### **#3-3 输入接口**

如果你细心一点，你会发现模块左侧的接口有多种颜色，这实际上告诉了我们接口是否必需接入内容。我们已经知道，Advanced Perlin等模块有多个输入接口。通常，非必要的输入接口起到的是引导作用。

我们常常把地形雏形接到Advanced Perlin的第一个接口，这是因为这个接口能引导噪声形态，让噪波更趋近于我们的原地形。我们现在尝试将一个Perlin接入另一个Perlin的第二接口，可以看到Perlin发生了一些类似Displacement模块效果的扭曲。我们进入模块参数页面，勾选Show advanced settings，进入Guide inputs选项卡，这里面的三个参数实际上就对应三个输入接口的引导能力。我们拉高Distortion guide level，扭曲程度就会变得越来越大。

了解各个模块输入接口的作用，对制作更精妙的地形有巨大帮助。

![](https://thingy.top/view.php/ee102e15252a11ef0d4c11d83ce3edcf.png)

![](https://thingy.top/view.php/55ed9e1469e6e179202739b702f52185.png)

### **#3-4 模块排列**

首先要明白一个原则——保留细节。这很容易，但是常常被忘记。例如我们已经有了一个有丰富纹理的山脉，但我们此时加上一个侵蚀，原有山脉的纹理全部被侵蚀破坏掉了，这显然不是我们想要的。

但还有一个例外的进阶做法，将地形塑形和纹理分开制作，手动抹去塑形过程中添加的纹理，再在后期重新添加纹理，这种做法难度过高，不做详细介绍。

![](https://thingy.top/view.php/bef390ad4c8c6acf901fb4bc4973f341.png)

其次是另一个原则——追根溯源。

比如我们地形变成这样了，一堆尖刺，我们不能想最后处理，而是要一个一个模块往回找，看看哪里出现了这种错误效果，找到问题模块并解决问题。例如此处我们应该在Multiply后加上Blur，这个问题此前在 #3-1-2 处理遮罩 中讲过。

![](https://thingy.top/view.php/1eeb435b386e8dad501eeec424861bea.png)

![](https://thingy.top/view.php/f87072d83c539d12d44efb75ed5b6413.png)

### **#3-5 打破定势**

很多新人都会陷入一个误区，被所谓的地形流程禁锢住，但实际上，流程只是一个参考，在制作过程中跳出限制更为重要。例如自然化模块就不必用于自然化处理上，模块归根到底都是一种算法，一种滤镜，不要被他的颜色迷惑住。例如 #2-1-2 自然化：风化（Thermal Weathering） 中的旧版风化模块，常常可以不拿来做自然化，而是参与地形的塑形阶段。

发现模块名字背后的隐藏用法十分重要，例如 #2-3-10 滤镜：水流重构/河道预处理（Flow Restructure） 中的这个模块除了介绍的这些效果，还可以用来进行快速造山，我们称之为河流造山法。需要注意的是Radial Grad画出的是山脉范围。

![](https://thingy.top/view.php/ef3ce801a270dd3cf782b2910e3c5d22.png)

![](https://thingy.top/view.php/661f19f5f5ccc542e531dc913ed822c1.png)

![](https://thingy.top/view.php/7b20d2e909ace7bc8cddc986c3e3619e.png)

# **第四章 基础效果**

本章节所有内容在WM工程内讲解，可以通过双击对应效果所在区域的Group框查看讲解。这部分讲解是次要的，重要之处在于看模块排列方法和模块参数。

工程文件下载链接：https://thingy.top/down.php/0780f09549a626d6e942fa04ee514da5.tmd

**#4-1 侧侵**

自上到下分别是不讲道理的次世代Strata方法，近代方法和远古方法。推荐前两种，第三种几乎已被废弃，仅在少数情况下效果突出，放在这只是因为他的历史价值。侧侵的重点在弄出这个侧向纹理来，因此几乎与位移操作相关的模块都可以拿来做侧侵。现代方法也可以将后一个combiner的模式切换成Screen，反正叠加纹理的方法无数种，哪个合适顺手就用哪个。

**#4-2 沙漠纹理高原**

沙漠纹理高原，我学地形的时候就有的东西，经典永流传系列的，流水的地形圈，铁打的沙漠纹理高原。需要注意的是，Displacement后的第一个Clamp把地形拉到了最高，后面接的一堆Clamp里最后一个是摆设，然后每一个Clamp自下而上压1/5，直到Constant处为0，这样可以保证阶梯化过程能将高原等分。

**#4-3 鳞片**

鳞片，很简单，没什么好说的。

**#4-4 硬山**

总有新人把做硬山当成什么世纪难题，但你看这么简单的单模块方法这随便就能列出来三个。

**#4-5 尖尖山**

尖尖山。第一个很简单，不再赘述。第二个需要较为深厚的理解才能明白，不理解也没关系，当成选学内容。主要思路是剔除初步处理的部分，剩余部分二次处理后，将两个部分叠加起来，这样做的原因是Expander模块处理的位置是根据坡度来的，这种方法可以保证山顶不走形。

**#4-6 奶油雪**

奶油雪。一个比较简单的迭代思想，先利用第一个Snow和Snowmelt选择出迭代区域，随后对这一区域进行迭代处理，也就是第二个Snow的参数拉的很高，让选区鼓起来，形成类似奶油的效果。最后加上一个普通雪，叠加遮罩，为迭代过程中没有上雪的部分添加雪。

**#4-7 水系**

最简单的水系制作方法，也许你觉得效果不够好，但是这个效果因为有了CreateWater模块的加入，爆杀了以前所有的方法。这个流程是固定的，记住就行。

如果你想尝试更为复杂的水系效果，可以看看这个视频和工程，这一部分属于进阶内容，需要极高的软件理解才能掌握。

教程视频

https://www.bilibili.com/video/BV1HU4y1V7Au?share_source=copy_web&vd_source=8535694fbcb3402017ff3a91e535a343

教程工程

https://thingy.top/down.php/d03c6c95d86d0b01a65b1846e1c8e230.tmd

这里还有一个投机取巧的方法，StylelessArc此前发布了一个河流宏，限于版权问题，请自行在下方的发布链接中获取。

https://stylelessarc.gumroad.com/l/braided-rivers

# **附录**

## **附录-1 地形圈指路牌**

衰变死猫的Worldmachine视频教程

https://space.bilibili.com/3164992/channel/seriesdetail?sid=983629

花开的WM启动问题处理文档

https://www.mcbbs.net/thread-1276091-1-2.html

花开的GAEA教程

https://www.mcbbs.net/thread-1301102-1-1.html

花开的Chunky汉化

https://www.mcbbs.net/thread-1246420-1-1.html

243的源石晶体制作教程

https://www.bilibili.com/video/BV1T7411k7V8

茶馆笔刷包

https://www.mcbbs.net/thread-1299394-1-1.html

茶馆下载站

http://thingy.top/

介介子的WM进阶视频教程

https://space.bilibili.com/231232390

Minecraft地形师茶馆

878646382

CTI中华地形师学会

199077727

花开的WM汉化群

854909057

黑霞的Terragen交流群

431201361

### **附录-2 后记**

你问我为什么上色一点没讲，因为WM给出了十分丰富的上色示例工程，包括我个人也不怎么会的PBR材质，所以建议直接去看示例工程。示例工程打开方式：左上角File-Open Example World。WM出来的遮罩要怎么用，这就该WP教程讲了（甩锅），本文默认你已经完成了Worldpainter的学习。至于WM出来的图片要怎么糊到地形上，这个确实不该WP教程讲，但是也有人写过了，参见黑霞《在WorldPainter中使用图片(Bitmap)上色的方法》（https://www.bilibili.com/read/cv15247110），上色脚本链接https://github.com/creativitRy/ColorToTerrain，该脚本在新版本WP可能失效，如失效可尝试修改版https://thingy.top/down.php/7939ed3a2303fafe9b07ef3035163d44.js。

地形学习长路漫漫，本文万字左右仅能达到入门目的，更高更妙的MC地形远不止于此，相信肯读完本文的各位都对地形制作十分感兴趣，期待你们能在地形这条不归路上继续走下去。技术并不决定地形效果，虽然不可否认技术对地形制作很有帮助，但只有你肯花时间反复打磨，愿意尝试将自己脑海里的无数遐想化作现实，绝对好过单纯技术的堆砌。地形作品效果的日益完美是能够看到的，这种能够看到的进步又会继续激励你向更远的地形路前行。

感谢你阅读完本文，希望本文能够对你有所启发。

最后，感谢本文引用内容的作者和在本文编纂过程中给予帮助的众多地形师和群体，包括但不限于：

花开

FN Studio

Minecraft地形师茶馆

CTI中华地形师协会

地形建模交流进步群

