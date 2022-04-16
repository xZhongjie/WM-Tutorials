# **第零章 我是 WM World Machine你学会了吗**

## **#0-0 序言**

## **#0-1 下载与安装**

World Machine是一款功能强大的地形建模软件，官网地址<https://www.world-machine.com/>。目前售价为社区版免费、独立开发者199美元、专业版299美元、工作室版1999美元。社区版限制较高，不推荐使用，本文不提供直接的破解版下载地址。您可以前往画忆妙妙屋等网站自行搜索。另外也推荐使用花开汉化的版本，群号为854909057。本贴使用版本为v4027 Professional 英文原版。安装后，如果遇到启动失败相关问题，可参考花开的解决文档<https://www.mcbbs.net/thread-1276091-1-1.html>。

## **#0-2 操作逻辑**

WM的操作逻辑是节点操作，一般地形制作流程为形体－调整－自然化－上色。这里仅做一个简单介绍，WM流程在第壹章会重点教授。一般称WM的节点为模块。WM的模块效果各异，但基本构造相同。

以图中模块为例，左侧为输入端，右侧为输出端，上方为数据接口（4027版本开始不再主动显示），下方为遮罩接口。简单来说，左侧接入的内容经过模块的处理后传给右方，这就是模块的工作原理。

需要注意的是，模块名称左侧还会亮起指示灯，青绿色表示正常工作，黄绿色表示尚未构建，蓝色表示已构建但内容已被删除，红色表示接入方法有误，红叉表示WM工作异常。

![](http://thingy.top/view.php/fcb265ff3b5ef00c370bd98a1d529204.png)

## **#0-3 基本操作**

开始之前，先简单将WM界面分个区，方便介绍。

![](http://thingy.top/view.php/e77227686b59d607684091f0d5cbded3.png)

模块栏：取模块的地方，没什么好说的。

预览区：大框里面显示的是当前模块预览效果，你可以修改下面的选项来调整光照，水体，描图等等效果。

模块陈列区：会显示出来你摆下的每一个模块。历史栏里可以保存你的操作记录。

工具栏：其实每一个有图标的选项都是文字选项卡里面比较重要的选项，这里只重点说一下下面那行有图标的。从左到右依次是新建工程、打开工程、打开示例工程（强烈推荐翻阅，有助于快速上手）、保存、导出页面、工程设置页面、WM设置页面、随机种子、显示/隐藏侧栏、修改工作布局、工作页面、布局界面、探索页面、3D预览、2D预览、构建全部模块、构建当前模块、分块构建。

至于右键模块弹出的窗口，这里直接借用花开汉化版的翻译，相关快捷键也有体现，不再赘述。

![未标题-1](http://thingy.top/view.php/70c3a0b444bc5ce32fe85573c8fe27f6.png)

## **#0-4 尺寸对应**

地形圈普遍认为，地形的1比1即指1方块等于10m。根据该规则，应将工程设置页面中的子选项卡Scene Setup中Width（或Breath）的值与Resolution的值设置为 x km 与 100x 。1k地形即指10.24km x 10.24km的地形，其他尺寸同理。例如Width为10.24km，Breath为10.24km，Resolution为1024x1024。这就是所说的1k地形。如果需要非正方形尺寸地形，只需要修改Square Aspect为Any Aspect Ratio。如果您的尺寸设置正确，Detail scale的值应为10.00m/pixel。WM默认的地形高度为4km（400方块），需要将Project Setup选项卡中Dimension Preference的值根据需要修改为2.56km（256方块）或3.84km（384方块）等等。

![](http://thingy.top/view.php/e1b2f048e163172c7de1c179f19ca589.png)

# 第一章 **年轻人的第一个WM工程**

## **#1-1 创建形体**

这里以制作一个2k山区为例，为大家介绍具体的WM地形制作流程。首先根据#0-4中所教，创建一个2k世界。

随后，我们可以在模块栏中Generator一栏，选择Advanced Perlin（高级柏林噪声）![](http://thingy.top/view.php/c3c9aebb26862c12a1866c8f47ce073a.png)，这是一个十分常用的模块。

我们就可以得到这样的性质，称之为噪波，这是多数地形的开始。

![](http://thingy.top/view.php/550a0dc4020804bf73a9720e63ecd267.png)

我们需要对其进行一些参数调整，双击模块，将Scale的值调到20km，适当修改Steepness和Middle elevation的值，得到这样的形状。大家不妨自行尝试，调整各个参数，以便了解参数对应的效果。

![](http://thingy.top/view.php/fbf97c6d68304667740e68095ba1ff8c.png)

## **#1-2 调整形状**

随后，拿出Filter栏中的Displacement![](http://thingy.top/view.php/405ceca14b97453d7d2fb30db82a4950.png)模块和Generator中的Basic Noise![](http://thingy.top/view.php/46072f39b97ff243db15935c8640d479.png)模块，以这种方式连接，对我们之前Advanced Perlin的地形进行一些扭曲。Displacement模块的Distance需要适当调整为1.5km左右，Direction视情况决定是否调整。

![](http://thingy.top/view.php/d2461f47e1e7faea2f6a98f63826b975.png)

![](http://thingy.top/view.php/ab5b73aef1647c735aaf2ecbae5ba49a.png)

## **#1-3-1 自然化处理：侵蚀**

再到Natural栏中找到Erosion（侵蚀）![](http://thingy.top/view.php/f16c3a9b1c4d24701e2ab6e5b41cf935.png)模块，连接到Displacement的后面。在右上角Presents栏中，选择Deeply Carved预设。WM自带的许多预设都十分好用。

![](http://thingy.top/view.php/941ee351fe30f5c69e9a4574c449fa4d.png) 

## **#1-? 随机应变**

我们终于获得了一个像山的形状，但这还不够，我们注意到一些地方由于侵蚀的效果，已经碰到了地形的底部。我们只需要再摆下一个Advanced Perlin模块，并找到Combiner中的Combiner![](http://thingy.top/view.php/6375e94e4ccb07b1ec82d5803ff20361.png)模块。将Advanced Perlin中的预设选择为Swiss Cheese，适当拉低Middle elevation的值，然后将Combiner的模式修改为Screen（防止地形顶破限高)，并将强度拉到1，并以这样的方式连接模块。可以看到地形碰底的问题已经得到解决。

![](http://thingy.top/view.php/0aa24cbcc0b6783922ee37e98d10be35.png)

![](http://thingy.top/view.php/7fdf8625b686533722ca5148ed845751.png)

## **#1-3-2 自然化处理：风化**

我们再到Natural栏中找到Thermal Weathering（热力风化）![](http://thingy.top/view.php/3955726ae2d322d3e13ce6a323c5bd1d.png)模块，直接接入即可。但是我们好像很难发现地形有了什么变化，不妨试着打开3D预览页面中的比较线![](http://thingy.top/view.php/1ee2dde29f8cc9a733d28dd64d78d0b1.png)，这样我们就可以直观看出地形前后差距了。可以发现，风化过后的地形，高坡度地区产生了一些碎石。

1![](http://thingy.top/view.php/a5657a3185c2305a64595a1ec272fe14.png)

## **#1-4 上色**

上色较为复杂，这里我们使用上色宏解决。找到工具栏中Macros（宏）一栏，找到Texturing中的Quick Texture摆下，接入后我们就可以快速得到地形上色。宏的本质是多个模块整合到一起，制作方法后续章节再讲。我们再找出View模块栏中的Overlay Preview![](http://thingy.top/view.php/e7c25e62cef2914915d1aa70da9f28cb.png)，上口接入地形，下口接入上色，预览效果。

![](http://thingy.top/view.php/e62b875489d99d4de2962f27828fa47a.png)

## **#1-5 导出**

我们的地形已经制作完成了。接下来找出Output栏中的，Height Output![](http://thingy.top/view.php/ffa2d4956b1681201d0205a1181f1d58.png)和Bitmap Output<img src="http://thingy.top/view.php/ec0e4e06ba14fecbbb80b09e6c7c2def.png" style="zoom:120%;" />，分别将地形和上色接进去，修改文件名。然后打开导出页面![](http://thingy.top/view.php/03c86c732ccc97f3c2f0ee4d0fe8e1b7.png)，选择Export All，我们就可以在显示的目录中找到保存好的两张图片。

![](http://thingy.top/view.php/23b4e28fa32897fe4aeb653e0bc2aa53.png)

# 第二章 **模块效果**

我们已经知道，做地形需要依靠模块的堆砌，那么为了做出更好的地形，我们有必要了解一下常用模块的效果。

## **#2-1 自然化**

自然化其实并不摆在模块栏的前列，但自然化效果对地形制作十分重要，因此我们第一个先讲自然化。

### **#2-1-1 自然化：侵蚀（Erosion）**

侵蚀是新手时期最重要的自然化模块。侵蚀的效果还是很显而易见的，可以看到我们的地形上出现了很明显的沟壑。

![](http://thingy.top/view.php/b6428d7e6d90f1c97884b740ac1e4ce3.png)

接下来简单介绍一下比较重要的参数。也许描述不是特别十分非常严谨，但是应该可能大概估计是足够新手使用了。

Duration（侵蚀时间）：数值越大效果越强。

Rock Hardness（岩石硬度）：数越大沟越深。

Sediment Carry Amount（泥沙量）：数越大沉积越重。

Geological-time Enhancement（冰川侵蚀/地质时间增强）：勾上了就会对地形主体以外的地方产生作用。

侵蚀模块有三个入口，第三个没啥用。

Hardness Mask：接入灰度图的值会乘上参数中的Rock Hardness，乘积来确定岩石的硬度。

侵蚀模块有四个出口，相信聪明的你大概看一下就懂了。Flow、Wear一般不译，Deposition一般称作沉积。

当然，作为一个地形圈资深养老人，我十分建议大家去试试WM给的参数，不必自己一个一个去调，在参数的基础上作出一点修改即可。比如Deeply Carved预设，我们适当拉低一些岩石硬度，直接就有硬山了。

![](http://thingy.top/view.php/e179349000577ba66588ac61d9c69f38.png)

### **#2-1-2 自然化：风化（Thermal Weathering）**

当你继续深入学习地形之后，你就会觉得------

侵蚀你就是歌姬吧，你来风化大街，指定没你好果汁吃嗷

![](http://thingy.top/view.php/8a69de679798477208e5b62d117e3bce.png)

Talus Production（碎石量）&Intensity（强度）：控制产生碎石的多少

Talus Repose Angle（碎石坡度）：如果坡度大于这个值，地形就会产生滑坡，在山脚形成碎石。

Fracture Size：屁用没有。只有在数值差异极端巨大的时候能观察到些许差异。他就跟语文老师讲的那个勾八课外文言文一样，出个死勾八难的实词结果这玩意是你这辈子最后一次见到，高考从来就没考过。

Talus Size（碎石尺寸）：数越大堆积坡越凹凸不平。

Simulation Length（碎石距离）：数越大碎石就滚得越远。

特别需要注意的是，这个模块他的旧版本也特别特别特别好用，这里不过多叙述，只提供给大家两张效果图和对应参数，读者自证不难。

![](http://thingy.top/view.php/d4b7a41aed36c51a58d05d1d6e4d8576.png)

![](http://thingy.top/view.php/5c1962a761757085296d4c6a415dfe29.png)

![](http://thingy.top/view.php/55d50aa038e62920581ba6c9de66b1c3.png)

![](http://thingy.top/view.php/1ccf481a91e8fd64d13e64575d2f3c41.png)

### **#2-1-3 自然化：地层（Strata）**

![](http://thingy.top/view.php/0cdba41acaf6a65d2214253ea38fddab.png)

你把它理解成阶梯化Pro Max就行，虽然我们还没接触阶梯化（

Strength（强度）：强度还能是什么意思。

Scale（范围）：数值越小分层越多。

Smoothness（模糊程度）：字面意思。

Layer（层化程度）：字面意思。

Tint（角度）：控制纹理的角度，因为容易和下一个参数弄混，所以干脆放图解释。

![](http://thingy.top/view.php/f1334f787e1ccf2552dcd8b989aa7851.png)

![](http://thingy.top/view.php/519eeec5e6feb245138c0b3c5b7b1089.png)

Heading（方向）：控制纹理倾斜方向，放图。

![](http://thingy.top/view.php/941d6cfd79b1d8f210af40847a691cbf.png)

![](http://thingy.top/view.php/26662b9109489d22e87d6959180a788a.png)

### **#2-1-4 自然化：雪（Snow）**

![](http://thingy.top/view.php/9fe0d833e61758810af596b7e10468bc.png)

Snowfall（降雪量）：值越大，雪对地形的平滑程度越高。

Stickiness（黏度）：值越大，雪的黏性越强，更容易黏在坡度高的地方。

Snowmelt Mask Input（融雪遮罩输入）：值越大，第三个输入端口接入的遮罩的范围内的雪融化越多。

这一模块可搭配Natural Effects类中的Snowmelt宏使用，辅助进行融雪。

### **#2-1-5 自然化：海岸侵蚀（Coast Erosion）**

这铸币模块属于是特别有用的，而且不可替代，但是实在是太铸币了，在WM的某次逆天改版之后，给的Water不是很精确，导致做水流的时候一堆破事。

![](http://thingy.top/view.php/e46410172e8f72bed8b4a207bf1898d2.png)

Sea Level（海面高度）：字面意思。点那个按钮可以自己对应场景设置的海平面高度。

Beach Size（海滩大小）：字面意思。海岸会从基础线开始向海里拓展。

Inland Height Influence（陆地影响程度）：和上面的海岸大小相反，修改这个参数，海岸会从基础线开始向陆地拓展。

Underwater Smoothing（水下平滑程度）：字面意思。

### **#2-1-6 自然化：Create Water**

这里只介绍参数，河流制作在后续会系统讲解。参数直接引用我进阶视频教程中的，懒狗了属于是。

![](http://thingy.top/view.php/e8990d654b9f53f1c04a7fb7a325349e.png)

![](http://thingy.top/view.php/ba4fc3f2d0af3598238629e47baf0e93.png)

## **#2-2 生成器**

**生成器是绝大多数地形的开始，也是许多流程中不可或缺的。**

### **#2-2-1 生成器：高级柏林噪波（Advanced Perlin）**

![](http://thingy.top/view.php/0e389779fcb3f899161015a9bc34e7dc.png)

接口方面，也就形状、扭曲、精度三个指导接口，挺简单的，指导强度在参数里面隐藏起来了，勾选上显示更多参数就显示了。参数简单介绍几个，因为我懒，直接贴一个3026 版本的模块界面汉化图。

Feature Scale：噪波规模。越小纹理越密集，地形凹凸起伏越多。

Style：噪波样式。

Persistence：叠加精度，越低噪波越圆润。

Lacunarity：叠加规模，也就是又叠上来的小噪波的Feature Scale。

Octaves：叠加数量，越高噪波越复杂。

Seed：随机种子。

Steepness：噪波起伏。

Middle Elevation：中位高度。

![](http://thingy.top/view.php/1ab67252db4d258340f441ac7d4da447.png)

![](http://thingy.top/view.php/610592e654ea6a3fd12589af3aee78ef.png)

### **#2-2-2 生成器：基础噪波（Basic Noise）**

和Adv Perlin大同小异，Style有点差别，不再赘述。

![](http://thingy.top/view.php/1045ba0dc873e0cc6dbd5e72462a3e94.png)

### **#2-2-3 生成器：Color**

颜色生成器是一种产生恒定颜色的简单模块。默认情况下，创建一个全图范围的单色。但是，通过使用遮罩输入或将输出与选择遮罩组合，颜色生成器将成为上色工作的基础。

### **#2-2-4 生成器：Constant**

常量生成器仅创建指定高度的水平平坦地形。

### **#2-2-5 生成器：File Input**

从外部导入地形的模块，应该没有什么好说的，调Type可以修改导入文件的类型，Width调长宽，一般来说知道这点就够了，也许你足够牛逼的时候还会接触到重采样方式，其他估计是永远用不到，但是3026版汉化依旧汉化了每一个选项，有需要可以看看。

![](http://thingy.top/view.php/c8187e32590f8b2a3b7bc45f53a05d81.png)

![](http://thingy.top/view.php/ea468680a678d46e6b1fdf8474c6297f.png)

### **#2-2-6 生成器：Gradient**

生成斜面用的模块。没什么好说的。Tilling里面四种模式，分别是硬边缘和软边缘的单个斜面，以及单面和镜像的多个斜面。

![](http://thingy.top/view.php/b67777ee46af88d9a80fb6b974d4071c.png)

### **#2-2-7 生成器：Radial Grad**

Radial Grad能创建一个简单的以空间中的一个点为中心的几何形状。

![](http://thingy.top/view.php/d03fc8f6924f9a0563622e1083c807a2.png)

这里我直接翻译了官方文档，然后补上一点官方文档没有的。

Radius（半径）：形状应覆盖多大的面积。默认值为8km，恰好完全填充了默认的地形范围。

Type（类型）：

球形Spherical:在边缘急剧下降的圆形轮廓。

高斯Gaussian:呈高斯分布的丘形轮廓。

钻石Diamond:看起来很像金字塔的不断倾斜的轮廓。

正方形Square:方形轮廓。它保持水平，直到边缘急剧下降到零为止。

锥形Cone:在所有方向上恒定向下倾斜到零。

指数Exponential：临近中心处下降快而边缘处下降慢，类似幂函数。

正弦Sinusoidal：在侧面看起来和正弦函数图像一样的形状。

圆锥横扫Conic Sweep：照着GAEA学的一个形状，长这个样子。

![](http://thingy.top/view.php/d8e2153bd93293b00219217ffc7e5ac4.png)

### **#2-2-8 生成器：Voronoi**

有些类似水波纹，十分重要的模块。

![](http://thingy.top/view.php/2dd68c0ad5d010643318630cb86470a4.png)

Feature Scale：规模。

Style：类型。这个模块的类型很多，可以自行尝试，需要注意的是他有几个生成类似麦田轮廓的细胞模式。

![](http://thingy.top/view.php/06e99dca2bf1c1c9dc2f5006168891e0.png)

Crystallize：打开之后模块只接受彩图，对彩图执行晶格化操作。

### **#2-2-9 生成器：Shapes**

十分重要的模块，做综合地形必不可少，旧版本名为Layout Generator。

双击之后，我们就会发现这个模块不会弹出参数窗口，而是直接跳进了布局页面。

![](http://thingy.top/view.php/774bc8e924326d922e59203f13e90926.png)

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

![](http://thingy.top/view.php/21d4818d2af97e153f5d7f8f28726fbd.png)

### **#2-3-2 滤镜：环境光遮蔽（Ambient Occlusion）**

在3028时代有个大神想要AO效果，于是用了360个角度的光照图叠出来了AO，官方看见之后连声叫好，正义制作了AO模块，只留下暴力大神在风中凌乱。

![](http://thingy.top/view.php/3f6965973acf0dbc92afb764b30fc225.png)

我之前录过一期视频教程（https://www.bilibili.com/video/BV19o4y1D7rF）专门讲这个模块的，有需要可以看看。

### **#2-3-3 滤镜：Bias/Gain**

地形圈有这么一句玩笑话，如果你想让你的地形看起来高端，就把Clamp换成Bias/Gain。这个模块的效果和Clamp的Rescale和Expand模式几乎一致，但是相对用的人少。用法和PS的亮度/对比度相同。

### **#2-3-4 滤镜：Blur**

效果是模糊，除了一般的高斯模块，这个模块还提供了径向模糊，修改Method的选项即可。

![](http://thingy.top/view.php/4db03aca0542445ae9716d648a7f71b1.png)

![](http://thingy.top/view.php/64ee4813dad164b448c130abc9111044.png)

### **#2-3-5 滤镜：Clamp**

十分重要的一个模块，可以压低/削顶/抬高地形，分别对应Operation的三个选项。

这个模块还提供了一个Find Extent的按钮，点击这个按钮，WM就会将Clamp的模式转为Expand，并自动帮你对应到地形的最低点和最高点，让地形占据整个高度范围。

### **#2-3-6 滤镜：晶格化（Crystallize）**

可以将地形转化为六边形或正方形的堆叠。4027新增的模块，还没有模块图标。

![](http://thingy.top/view.php/f00fa39e411fc9a4d6e26e2b06cc46a1.png)

### **#2-3-7 滤镜：曲线（Curve）**

和你在PS里面用的曲线一样的，没什么可说的。对于新人十分难以控制，不推荐。

![](http://thingy.top/view.php/e888bdcf78c74279b27d6920852ca416.png)

### **#2-3-8 滤镜：Displacement**

特别特别重要的一个模块，可以对图像进行位移操作，或者俗称是扭一扭。第二个接口必须接东西，Vector模式下第三个接口也必须接东西。而且你会发现，伴随着Type的变化，端口的名字也会发生变化。

![](http://thingy.top/view.php/b754a0113e1aa6621fc54ba42c929c43.png)

Type：

Angle And Distance，你可以简单理解为，把第一个端口的地形往第二个端口的形状去扭，第三个端口做引导，有没有都无所谓。

Vector模式下，第二个接口控制X怎么扭，第三个接口控制Y怎么扭。

这样的说法及其不正确，只是为了方便理解。

Direction：控制位移的方向。

Distance：控制位移的距离。

### **#2-3-9 滤镜：Equalizer**

屁用没有。

但是有点屁用，在一些遮罩，比如Snow的Snow Mask遮罩里面，一些地方及其不突出导致你预览起来和到WP里面刷的雪是两回事，这时候只要接入Equalizer，就能让原本不明显的地方突出起来，以便我们进行下一步过滤。

![](http://thingy.top/view.php/a0fb69d2b04d21718845d67678736777.png)

### **#2-3-10 滤镜：水流重构/河道预处理（Flow Restructure）**

字面意思，能有效解决Create Water的断流问题，水系问题后面会系统地讲，目前你只需要知道，这个模块可以来开一些大型的河道，让地形的高低落差能够实现水流畅通而不是堵成湖泊。

### **#2-3-11 滤镜：Expander**

对地形进行扩张，处理遮罩和造山的利器。

![](http://thingy.top/view.php/cbddceee20b57d41ce7cc26312d54d94.png)

Action：扩张方式，Expand向外扩张，Shrink向内收缩，Open和Close夹在两者之间，Close更靠近Expand，Open更靠近Shrink。

Type：扩张种类，分别是高斯（类似圆形）、线性坡度（类似棱锥）和方块。

Distance：扩张程度。

这个模块还有一个旧版本，WM2.x有Circle模式的扩张，十分好用。

![](http://thingy.top/view.php/ca2bf6bb2a373708b345834a9173649b.png)

### **#2-3-12 滤镜：Flipper**

翻转。有时候你好不容易画出来好看的大陆架，但是发现方向错了，一正过来不那么好看了，就可以翻转一下。不太常用。

### **#2-3-13 滤镜：Inverter**

反相。

### **#2-3-14 滤镜：概率（Probability）**

![](http://thingy.top/view.php/9f570c99d3468b93a70353317811afea.png)

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

![](http://thingy.top/view.php/a704d3b1c313e26394b16496ab44381f.png)

### **#2-3-16 滤镜：Simple Transform**

功能十分丰富的一个模块，可以实现各种简单的高度调整。效果强度由Intensity控制。

### **#2-3-17 滤镜：阶梯化（Terrace）**

![](http://thingy.top/view.php/968977eb5914d2c6ad52548a35e72053.png)

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

Max：保留最大值。

Min：保留最小值。

### **#2-4-2 Multi Chooser**

将地形按照高度分为多个小块后，在对应高度使用对应接口的地形进行操作。可以实现阶梯化效果。

Number Of Inputs：输入接口和分层的数量。

Transition Contrast：可以简单理解为阶梯化程度，这样说并不准确。

图片中，我将接口数量设置为2，在第一个接口连接了高低落差很大的噪波，第二个接口接入平面，第三个接口接入Voronoi。可以看到高度高的地方变为了Voronoi，而高度低的地方变成了平面。

![](http://thingy.top/view.php/8da27a6a871efd613658f1a0e65927d6.png)

## **#2-5 选择器**

选择器可以帮助你选择出各种遮罩以便限定模块操作范围。模块颜色为紫色。

### **#2-5-1 选择器：光照角选择（Select Aspect）**

![](http://thingy.top/view.php/fcafb6022a83ecd1ca04b5f61ef739ae.png)

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

![](http://thingy.top/view.php/be08f6e637f4f77999a22dbaa1dd9138.png)

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
