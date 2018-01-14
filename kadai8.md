# 課題8

ORG=imread('images/cat2.jpg');  
ORG= rgb2gray(ORG);  
imagesc(ORG); colormap(gray); colorbar;  
pause;  

によって原画像を読み込み，グレースケールで表示した結果を図１に示す。  

![kadai8-1](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai8-1.jpg)
<div align="center">
図１ 原画像のグレースケール  
</div> 

IMG = ORG > 128;  
imagesc(IMG); colormap(gray); colorbar;  

によって閾値で二値化し画像を表示する。  

![kadai8-2](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai8-2.jpg)
<div align="center">
図２ 二値化した画像
</div> 

IMG = bwlabeln(IMG);  
imagesc(IMG); colormap(jet); colorbar;  

によって二値化した画像にjetのカラーマップでラベリングを行い次のように表示した。

![kadai8-3](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai8-3.jpg)
<div align="center">
図３ ラベリング後の画像
</div> 
