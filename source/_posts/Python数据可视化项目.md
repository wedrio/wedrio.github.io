---
title: Python数据可视化项目
date: 2020-05-21 08:58:14
tags: 
- 大数据
- python
categories:
- python
---
> 前提：安装matplotlib
<!--more-->
## 绘制简单的折线图
### 使用plot()绘制
		例：import matplotlib.pyplot as plt
			input_values = [1,2,3,4,5]
			squares = [1,4,9,16,25]
			plt.plot(input_values,squares,linewidth=5)

			#设置图标标题，并给坐标轴加上标签
			plt.title("Square Numbers", fontsize=24)
			plt.xlabel("Value", fontsize=14)
			plt.ylabel("Square of Value", fontsize=14)

			#设置刻度标记的大小
			plt.tick_params(axis='both',labelsize=14)

			plt.show()
linewidth决定了plot()绘制线条的粗细。函数tick_params()设置了刻度的样式。  
![](https://cdn.jsdelivr.net/gh/wedrio/ImageHosting/wedrio-pic/plot_01.png)
### 使用scatter()绘制散点图并设置其样式
<strong>绘制单个点</strong>

			import matplotlib.pyplot as plt  
			plt.scatter(2, 4, s=200)  
			#设置图表标题并给坐标轴加上标签  
			plt.title("Square Numbers", fontsize=24)  plt.xlabel("Value", fontsize=14)  
			plt.ylabel("Square of Value", fontsize=14)  
			# 设置刻度标记的大小  
			plt.tick_params(axis='both', which='major', labelsize=14)  
			plt.show()
s=表示点的大小  
<strong>绘制多个点</strong>

			import matplotlib.pyplot as plt  
			x_values = [1, 2, 3, 4, 5] 
			y_values = [1, 4, 9, 16, 25]
			plt.scatter(x_values,y_values,s=100)  

			#设置图表标题并给坐标轴加上标签  
			plt.title("Square Numbers", fontsize=24)  plt.xlabel("Value", fontsize=14)  
			plt.ylabel("Square of Value", fontsize=14) 
   
			plt.show()
![](https://cdn.jsdelivr.net/gh/wedrio/ImageHosting/wedrio-pic/scatter_1.png)  
<strong>自动计算数据</strong>  
利用list(range(x,y))生成区间的数  
然后赋值给x轴，再遍历这个列表并给y轴赋值  
再利用axis()给坐标

			例子：x_values = list(range(1,10001))
				 y_values = [x**2 for x in x_values]

				 plt.axis([0,1100,0,1100000])
<strong>删除数据点的轮廓</strong>  
调用scatter()时传递实参edgecolor='none'  
<strong>自定义颜色</strong>  
可向scatter()传递参数c=''  
也可以使用RGB颜色模式自定义颜色，可传递参数c=(0,0,0) ，并将其设置为一个元组，其中包含三个0~1之间的小数值，它们分别表示红色、绿色和蓝色分量。  
<strong>使用颜色映射</strong>  
利用y值设置颜色c=y-values,cmap=plt.cm.Blues   
python中所有的颜色映射，<http://matplotlib.org/>,单击Examples，向下滚动到Color Examples，再单击colormaps_reference。  
### 自动保存图表
plt.savegfig('xxx.png',bbox_inches='tight')  
第二个实参指定将图表多余的空白区域裁剪掉，保留则省略。