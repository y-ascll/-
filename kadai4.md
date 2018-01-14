# 課題4

ORG=imread('images/cat1.jpg');  
ORG= rgb2gray(ORG);  
imagesc(ORG); colormap(gray); colorbar;  
pause;  

によって原画像を読み込み，グレースケールで表示した結果を図１に示す。  

![kadai4-1](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai4-1.jpg)
<div align="center">
図１ 原画像のグレースケール  
</div> 

imhist(ORG);  
によってヒストグラムを表示する。  
![kadai4-2](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai4-2.jpg)
<div align="center">
図２ ヒストグラム  
</div> 
