BMFONT使用方法说明
			———— Created by zhoufeitian 2018-10-25
---

# 原理简要说明
  我们通过操作 BMFONT 程序来得到想要的位图字体，获得了两个文件（.png格式 和 .fnt格式），一个资源文件（.png）一个是配置文件（.fnt），
  配置文件根据文字的码来读取图片，配置文件有改字的几个基本属性，在资源文件中的位置（x，y），空间大小（width，height），上下左右偏移量。
  <font color = red>最最重要的是读取的id 即转换成把文字转换成机器可读的码</font>，这样我们就可以书写配置文件包含的文字来获取想要的位图字体了。

# 方法步骤
1. 将要输入的文字写到一个.txt格式的文件中，一定要保存为 UTF-8 格式！一定要保存为 UTF-8 格式！一定要保存为 UTF-8 格式！
![img1](https://github.com/17864117575/ScreenShot/blob/master/TIM%E6%88%AA%E5%9B%BE20181025121407.png?raw=true)
【图一】
2. 打开	_BMFONT.EXE_ 依次选择 Edit --> Select All chars[选择所有字] 和 Edit --> Clear All chars in font[在字库中清空所有字]，
   这一步的目的是为了将之前所有的添加的文字清除，建议在进行导入新字体之前都进行此步骤。
3. 选择 Edit --> Select chars from files[从文件中选择字]，打开刚刚写好的文件，然后选择 Options --> Save Bitmap font as...[将字体文件保存为..]
4. 在你选择的文件中会得到一个	.fnt 文件，该文件就是你之前写好的文件导出的，然后打开，该.fnt文件中 id 字段就是我们要的转换码，排列的顺序与之前.txt格式
   的文件字的顺序一致，我们获取该 id。
![img2](https://github.com/17864117575/ScreenShot/blob/master/TIM%E6%88%AA%E5%9B%BE20181025142550.png?raw=true)
【图二】
5. 然后重复 2. 
6. 选择 Edit --> Open Image Manager，弹出 Image Manager 之后，选择 Image --> Import Image..[导入图片]，选择要导入的图片。截图中标出ID 是之前
   我们记住的那些id。  
![img3](https://github.com/17864117575/ScreenShot/blob/master/TIM%E6%88%AA%E5%9B%BE20181025144447.png?raw=true)
【图三】
7. 将想要的图片全部导入完，查看一下 Options --> Visualize[视图预览]，确认无误后 Options --> Save Bitmap font as...
8. 最后打开 .fnt，保证里面的 files 字段与刚刚生成的 .png 格式的图片名称相同（如【图三】所示）