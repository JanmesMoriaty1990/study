study
=====

study
#高级教程：如何用MakeVT制作虚拟漫游
###内容


- [1、全景类型](#a)
- [2、热点](#b)
	- [a、什么是热点](#b1)
	- [b、图片热点的制作](#b2)
	- [c、多边形热点的制作](#b3)
	- [d、热点类型](#b4)
		- [过渡](#b41)
		- [图片展示](#b42)
		- [文本/超文本展示](#b43)
		- [链接](#b44)
		- [提示](#b45)
- [3、如何嵌入到Tumblr](#c)
- [4、发布后的操作](#d)
	- [a、发布后全景漫游的排列](#d1)
	- [b、krpano许可](#d2)
	- [c、main.xml的排列](#d3)
	- [d、如何编辑xml配置文件](#d4)
	- [e、如何删除logo](#d5)
	- [f、增加导航地图](#d6)
		- [添加地图图片](#d61)
		- [在地图上添加点击事件的热点](#d62)
		- [如何将热点在地图的x/y坐标上标示，并加以协调](#d62)
	- [g、在虚拟漫游上添加插件](#d7)
		- [组合框](#d71)
		- [单选框](#d71)
		
<a name="a"></a>
##全景类型

MakeVT当前版本只支持球面和圆柱形的全景制作。制作球面形的全景其图形必须是2：1的像素比例。如果全集图的像素是其它的比例，那么该全景图将会以圆柱形的类型加载。文件的格式是jpg，最大尺寸为50Mb。

<a name="b"></a>
##热点
<a name="b1"></a>
###什么是热点？

热点是全景上通过鼠标悬浮或点击而产生效果的区域。
热点有两种：多边形热点和图片热点。
MakeVT上的热点有以下几个用途：


1）加载新全景（过渡）；

2）显示在全景窗口上弹出的图片（图片展示的）；

3）在全景窗口上显示文本或是超文本（文本/超文本展示）；

4）链接到其他网站（链接）；

5）显示提示信息（提示）。
<a name="b2"></a>	
###图片热点制作


1、在热点编辑区选择一张在网页左侧列表中的全景图，然后点击“添加热点”按钮或键盘上的空格键。此时你已经开启热点添加模式，可以开始制作多边形和图片热点了；

2、在全景上点击你想放置图形热点的地方，点击的位置上将出现一个圆形图标。如果你想改变热点放置的位置，你可以单击“撤销最后一步”按钮或是键盘上的“Q”键，然后选择新的放置位置；

3、单击“保存热点按钮”，此时开启了热点设置窗口，你可以再该窗口中选择其他热点图标；在提示信息文本框中输入你想提示的信息，这些信息将会在鼠标悬浮在热点图标上时显示（该提示信息是可选的，你可以不填）；选择热点的类型，并设置必要参数；

4、点击“提交”保存热点设置。
<a name="b3"></a>
###多边形热点制作

多边形热点是全景上的一个多边形区域形成的热点。制作多边形热点和制作图形热点相似，所有的操作步骤都一样。唯一的区别是多边形区域代替了图标。操作步骤不下：


1、在热点编辑区点击“添加热点”按钮，进入热点添加模式，开始制作多边形和图片热点；

2、在全景上点击你想绘制多边形热点起点的地方，点击的位置将出现一个圆形图标。通过点击的方式你可以绘制出一个多边形区域。你可以通过单击“撤销最后一步”按钮或键盘上的“Q”键取消最近一步；

3、单击“保存热点”按钮，此时会开启热点设置窗口，你可以进行如下设置：在提示信息文本框中输入你想提示的信息，这些信息将会在鼠标悬浮在热点图标上时显示（该提示信息是可选的，你可以不填）；选择热点类型并设置所有必填参数；

4、点击“提交”保存热点设置。
<a name="b4"></a>
###热点类型

热点类型指示了你点击热点区域时所展示的效果。图片和多边形热点可以是以下五种可用类型中的一种：


过渡

图片展示

文本/超文本展示

链接

提示

所有的热点类型都有一个共同事件，即当鼠标经过热点区域时，其文本提示信息显示在屏幕的顶部。
<a name="b41"></a>
###过渡

点击热点后加载到另一个全景。

用户需要进行以下操作：

	1、选择要加载的全景；
	2、设置新全景的初始视角。该操作非常便捷，你只需将窗口上方的“眼睛”图标拖到与初始视角中心相对应的位置即可；
	3、设置全景的视角范围（范围为10到120之间）。
<a name="b42"></a>
###图片

点击热点后将在弹出框里展示图片。用户可以设置弹出框的宽度和高度像素。点击图片可以关闭弹出框。
用户需要进行一下操作：

	1、上传图片，图片格式为jpg，尺寸小于5MB；
	2、设置窗口的宽度和高度像素。
<a name="b43"></a>
###文本/超文本

点击热点后将弹出文本信息框。窗口大小根据屏幕的大小改变（其展示方式为：屏幕高度的64%，屏幕宽度的54%），用户无法改变这些值。如果文本信息超出窗口范围而不能完全展示时，窗口将会自动出现水平滚动条。你可以点击窗口右上角的关闭按钮关闭窗口。

你可以用超文本标记语言设计文本的结构。如果写出的文本信息没有任何标记标签，该文本将只显示在一段中（默认字体为Arial，文字大小为19像素）。

注意：Flash播放器并不支持所有的HTML/CSS标签。

所有的文本默认字体为Arial。

下面列出了一些常用的标记标签：

	1、<h>...</h>——新标题（文字大小为23像素，文本位置为居中）；
	2、<sh>...</sh>——子标题（文字大小为20像素）；
	3、<p>...</p>——新段落（文字大小为19像素）；
	4、<br/>——水平分割线，可以插入到段落之间的空行中，如：<p>...</p><br/><p>...</p>;
	5、<a href="url">Link text</a>——可以在文本插入一个其他网址的链接或是书签链接；
	6、<b>...</b>——将文字设为粗体；<i>...</i>——设为斜体；<u>...</u>——设置下划线。
<a name="b44"></a>
###链接

点击链接热点将弹出一个新的浏览器窗口，并在新窗口中展示其他网页信息。
<a name="b45"></a>
###提示

点击该热点不会执行任何事件。唯一的作用是在鼠标经过热点区域时，其提示信息以文本的形式显示在屏幕的顶部。
<a name="c"></a>
##如何在Tumblr中嵌入全景

打开Tumblr的dashboard（单击首页的左上角按钮，进入新页面后点击右上角的dashboard按钮），选择点击文本输入按钮，点击输入框上方的工具栏中的“html”按钮，弹出一个html文本的输入区域，在MakeVT的全景编辑的输出页面复制出自动生成的iframe代码，将该代码粘贴到html输入框。

为了使你的全景能更协调地嵌入Tumblr的展示模版，你可以适当改变代码中width（宽度）和height（高度）参数的值。一般调整为如下尺寸：width="500" height="390"。

<a name="d"></a>
##发布后的操作
<a name="d1"></a>
###发布后全景的排列

在确认发布全景漫游后，你会得到一个压缩文档。该文档包含了所有的运行和浏览该全景的必要文件（除了krpano的许可文件）。

###文件列表：


1、index.html——双击该文件，可以开始浏览全景漫游；

2、krpano.swf——krpano的flash播放器；

3、main.xml——xml配置文件，保存了用于配置各全景的XML标签。该文件描述了全景漫游的所有详细信息：图片路径，全景的基本信息和图标，热点坐标，等等；具体参考XML使用手册；

4、swfkrpano.js——rpano将编辑脚本嵌入到网页中。该脚本能自动完成许多操作，且能与大多数浏览器和系统兼容；详情请参考swfkrpano.js。

###文件夹列表：


1、plugins——krpano的插件，用于弹出文本窗口；

2、skin——该文件夹包含以下内容：

defaultskin.xml——xml文件，用于存储设计和功能的控制模块：鼠标捕获，控制按钮，全景的设计参数；

buttons.png——控制按钮的原图；

drag-cursors.png,qtvr-cursors.png——鼠标捕获时的按钮的原图。

3、tiles——全景预览和展示；

4、touricons——图片热点的图标；

5、toursimages——全景漫游中的jpg格式的图片。
<a name="d2"></a>	
###krpano许可证

Krpano Panorama Viewer是一个收费的全景制作工具。你在使用时必须购买它的许可授权。在你浏览全景漫游或是给全景图进行切割（全景被切割成许多小图，并逐张加载）时都需要用到krpano的许可证。

###发布全景漫游

我们没有将krpano许可证嵌入到发布的全景中，所以当你浏览下载的全景漫游时，你会在屏幕的中心位置看到一个krpano的模版水印。

如果你有krpano许可证，只需将该许可证和全景漫游制作文件放在同一文件夹（本地krpano.swf所在目录）下即可。

如果你没有krpano许可证，你可以krpano的官网（krpano.com）上购买。

###分享全景漫游

分享嵌入了许可证的全景漫游可以不用krpano的模版水印，但是如果没有许可证，水印会显示在屏幕的底部。
<a name="d3"></a>
###main.xml的配置

	<krpano version="1.0.8" onstart="loadscene(first_scene);">

	<!--全景连接文件, 实现了全景全局控制, 
	  按钮和鼠标的功能表, 跳转按钮, 
	  全景的预览视图-->
	<include url="skin/defaultskin.xml"/>

	<!--提示信息文本的默认样式-->
	<textstyle name="infostyle"  ...   />

	<!--设置所有全景-->
	<scene name="first_scene">
				  ...
	</scene>
				  ...
	<scene name=”last_scene”>
				  ...
	</scene>
	<!--关闭全景设置标签-->

	<!--文本输入插件的css样式-->
	<data name="css">
			 ...
	</data>
	</krpano>
<a name="d4"></a>
###如何编辑xml文件

你可能用普通的文本编辑器编辑过xml文件。但使用一些特殊的免费或收费的xml编辑器能更便捷地编辑xml文件，因为这些编辑器会有语法高亮显示，每行都会有数字编号标注，等等。

对于初学者，我们推荐使用简单且免费的xml编辑器，即XML Copy Editor。对于要求较高的，你可以根据需要选择xml编辑器。
<a name="d5"></a>
###如何删除logo？

发布全景后，你可能会马上想删除屏幕中间的logo。为此，你必须打开main.xml文件进行编辑。

打开main.xml文件后，你需要删除该配置文件中的两个插件：

MakeVT的logo（左下角）：

		<plugin name="tourmaker_logo"
			  url="%SWFPATH%/skin/tourmaker_logo.png" 
			  keep="true"  
			  align="leftbottom" x="3"  y="3" 
			  alpha="0.95" handcursor="true"
			  enabled="true" capture="false" 
			  edge="leftbottom"
			  scalechildren="true"
			  width="124"
			  height="30"
			  onclick="openurl(http://www.makevt.com/,_blank);"
		/>

Krpano的logo（右下角）：

		<plugin name="krpano_logo"
			  url="%SWFPATH%/skin/krpano_logo.png" 
			  keep="true"  
			  align="rightbottom" x="3"  y="3" 
			  alpha="0.95" handcursor="true"
			  enabled="true" capture="false"  
			  edge="rightbottom"
			  scalechildren="true"
			  width="154"
			  height="16"
			  onclick="openurl(http://www.krpano.com/,_blank);"
		/>

删除以上两个插件，保存修改，点击浏览查看。

但是在屏幕的中间依旧保留着krpano的水印——“krpano demo version”。若想删除该水印，你必须先得到krpano许可证（可以从krpano官网上购买），然后将该许可证复制到全景制作文件的同目录下。
<a name="d6"></a>
###添加导航地图

下面的例子展示了全景位置动态点的地图。如果你点击这些动态点，屏幕中会加载相对应的全景。地图有两个状态——大窗口和小窗口。你可以通过点击地图改变他们的状态。
<a name="d61"></a>
###增加地图的图片

让我们创建一个简单的地图。你可以通过点击它改变地图的尺寸（大窗口或小窗口）：


1、创建一个名为“map”的文件夹；

2、在“map”文件夹中放入一张地图的图片（如“map.png”）;

3、用xml编辑器打开“main.xml”文件，然后复制下面例子中的代码。
		例：
			<!--Map-->
			<plugin name="map" 
					 url="map/map.png" 
					 keep="true"
					 align="rightbottom" 
					 x="20"  y="20" 
					 alpha="0.95"
					 handcursor="false" 
					 edge="rightbottom"
					 scalechildren="true"
					 width="prop"
					 height="20%"
					 onclick="action(openmap);"
					 /> 

			<!--该操作使地图变小，即小窗口状态-->
			<action name="closemap">
					 plugin[map].changeorigin(rightbottom,rightbottom);
					 tween(plugin[map].height,20%);
					 set(plugin[map].onclick,action(openmap););
			</action>


			<!--该操作使地图变大，即大窗口状态-->
			<action name="openmap">
					 plugin[map].changeorigin(rightbottom,rightbottom);
					 tween(plugin[map].height,80%);
					 set(plugin[map].onclick,action(closemap););
			</action>
这个例子在屏幕的左下角创建了一个尺寸较小的地图（小窗口状态：高度为屏幕高度的20%；宽度根据“map.png”的宽高比自适应）。如果你单击该地图，它会变大（大窗口状态：高度为屏幕的80%，宽度根据“map.png”宽高比自适应）。如果你改变浏览器的尺寸，地图的大小也会随之改变。
<a name="d62"></a>
###如何识别与x/y坐标相对应的动态点？

以下介绍如何设置地图定位点的x和y坐标的属性。

坐标系：
	

起点——图片“map.png”的左上角；

x坐标的轴线——向右，y坐标的轴线——向下；

x坐标从0到map.png图片的原宽度像素之间变化；

y坐标从0到map.png图片的原高度像素之间变化。

注意：你必须使用map.png的原始尺寸，而不是大窗口状态或小窗口状态的尺寸。

例如，map.png的原始图为640*480.例子中的动态点将会在左上角（mappoint_1）和右下角（mappoint_2）。

为了识别x和y坐标，你可以使用图形绘制工具，这样可以显示相应的鼠标光标位置。你可以在Photoshop中处理。注意使用与系统相兼容的工具。
<a name="d7"></a>
###在全景漫游中添加插件
<a name="d71"></a>
###组合框

组合框插件添加下拉列表做成组合框。下拉列表中每个选项可以有不同的功能，在大多数案例中用于陈列全景跳转的链接。

1、下载combobox.swf,并添加到plugins文件夹中；

2、在xml编辑器中打开main.xml文件，并设置组合框的位置和每个选项的功能。

	例：
		<!--Combobox-->
		<plugin name="combobox"
				 url="plugins/combobox.swf"
				 align="lefttop" 
				 x="10" 
				 y="10" 
				 width="200"
				 height="20"
				 visible="true"
				 keep="true"
				 alpha="1"
				 />
		<!--Items of list-->
		<action name="combobox:Scene 1">
			   loadscene(my_scene_1);lookat(0,0,90);
		</action>
		<action name="combobox:Scene 2">
			   loadscene(my_scene_2);lookat(-10,-10,90);
		</action>




		
		
