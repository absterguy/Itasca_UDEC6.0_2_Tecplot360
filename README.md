# 导出UDEC6.0结果到Tecplot360进行后处理(UDEC2Tecplot)
(This is used to export the model results of the two-dimensional DEM software(UDEC6.0) to Tecplot360 for display and post-processing)

## 1.起因
UDEC6.0对模型计算结果的显示效果比较糟糕，导出的图的效果也糟糕。

前段时间有小伙伴问我后处理的问题，周末有些空闲时间，于是我看了一下Tecplot360的文件格式，参考了一些网上的转化程序，写了一个UDEC6.0的小脚本，帮助将UDEC6.0的模型计算结果输出为Tecplot360的输入格式。从Tecplot360可以很好的输出高质量图形，适合毕业论文和期刊论文使用。

最初网上有一个UDEC2Tecplot脚本是基于Tecplot旧版本的，而且我发现其中对应力的计算和输出是错误的，输出绘制的应力与UDEC中的显示结果不一样。

于是，我重新改写了程序(几乎重写了)，经过测试，脚本可以很好的转换模型的计算结果，包括节点位移、速度以及单元应力。

## 2.如何使用
当UDEC6.0中计算完模型以后，拷贝**UDEC2Tecplot360_shine_v3.dat**文件到当前的工程文件夹，并调用此文件：
```
call UDEC2Tecplot360_shine_v3.dat
```
该脚本将生成一个名为**udec_tec360_v3.dat**的文件，使用Tecplot360进行读取并显示

## 3.对比图

下面放几张对比图：UDEC6.0显示结果与Tecplot360的显示结果对比

**SYY**

![UDEC2Tecplot](https://image.geomatlab.com/image/20210620200114.png)

![UDEC2Tecplot](https://image.geomatlab.com/image/20210620201325.png)

**X-Disp**

![UDEC2Tecplot](https://image.geomatlab.com/image/20210620201452.png)

![](https://image.geomatlab.com/image/20210620201607.png)

**MAG-Disp&Disp Vector**

![UDEC2Tecplot](https://image.geomatlab.com/image/20210620201803.png)

![UDEC2Tecplot](https://image.geomatlab.com/image/20210620201935.png)

**Y-Vel**

![UDEC2Tecplot](https://image.geomatlab.com/image/20210620202048.png)

![UDEC2Tecplot](https://image.geomatlab.com/image/20210620202133.png)

**Mesh**

![UDEC2Tecplot](https://image.geomatlab.com/image/20210620203159.png)

![UDEC2Tecplot](https://image.geomatlab.com/image/20210620203252.png)
**SYY**

![UDEC2Tecplot](https://image.geomatlab.com/image/20210620203337.png)

![UDEC2Tecplot](https://image.geomatlab.com/image/20210620203518.png)
**Y-Disp**

![UDEC2Tecplot](https://image.geomatlab.com/image/20210620203743.png)

![UDEC2Tecplot](https://image.geomatlab.com/image/20210620203827.png)
**Y-Disp&Y-Disp Vector**

![UDEC2Tecplot](https://image.geomatlab.com/image/20210620204047.png)

![UDEC2Tecplot](https://image.geomatlab.com/image/20210620204119.png)

