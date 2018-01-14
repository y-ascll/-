# 課題6

ORG=imread('images/cat1.jpg');  
ORG= rgb2gray(ORG);  
imagesc(ORG); colormap(gray); colorbar;  
pause;  

によって原画像を読み込み，グレースケールで表示した結果を図１に示す。  

![kadai6-1](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai6-1.jpg)
<div align="center">
図１ 原画像のグレースケール  
</div> 


IMG = ORG>128;  
imagesc(IMG); colormap(gray); colorbar;  
pause;

によって128の閾値で二値化し表示した画像は次のようになった。  
![kadai6-2](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai6-2.jpg)
<div align="center">
図２ 閾値で二値化した画像  
</div> 

IMG = dither(ORG);  
imagesc(IMG); colormap(gray); colorbar;

によってディザ法で二値化し表示した画像は次のようになった。  
![kadai6-3](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai6-3.jpg)
<div align="center">
図３ ディザ法で二値化した画像  
</div> 
