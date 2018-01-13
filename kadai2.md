# 課題２

ORG=imread('images/cat1.jpg');  
ORG = rgb2gray(ORG); colormap(gray);  
imagesc(ORG); axis image;  

によって原画像を読み込み，グレースケールで表示した結果を図１に示す。
![kadai2-1](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai2-1.jpg)
<div align="center">
図１ 原画像のグレースケール
</div>
  
IMG = ORG>128;  
imagesc(IMG); colormap(gray); colorbar; axis image;  
pause;  

によって２階調画像を生成する。
![kadai2-2](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai2-2.jpg)
<div align="center">
図２ ２階調画像  
</div>  

IMG0 = ORG>64;  
IMG1 = ORG>128;  
IMG2 = ORG>192;  
IMG = IMG0 + IMG1 + IMG2;  
imagesc(IMG); colormap(gray); colorbar;  axis image;  

によって４階調画像を生成する。
![kadai2-3](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai2-3.jpg)
<div align="center">
図３ ４階調画像  
</div>  
  
IMG0 = ORG>32;  
IMG1 = ORG>64;  
IMG2 = ORG>128;  
IMG3 = ORG>192;  
IMG4 = ORG>224;  
IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4;  
imagesc(IMG); colormap(gray); colorbar;  axis image;  
pause;  

８階調画像はこのように生成した。
![kadai2-4](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai2-4.jpg)
<div align="center">
図４ ８階調画像  
</div>  
