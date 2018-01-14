# 課題３

ORG=imread('images/cat1.jpg');  
ORG= rgb2gray(ORG);  
imagesc(ORG); colormap(gray); colorbar;  
pause;

によって原画像を読み込み，グレースケールで表示した結果を図１に示す。

![kadai3-1](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai3-1.jpg)
<div align="center">
図１ 原画像のグレースケール  
</div>  


IMG = ORG > 64; % 輝度値が64以上の画素を1，その他を0に変換  
imagesc(IMG); colormap(gray); colorbar;  
pause;  

によって輝度値が64以上の画素を1，それ以外を0に変換する。  
![kadai3-2](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai3-2.jpg)
<div align="center">
図２ 閾値64  
</div>  


同様に閾値が96，128，196の場合を図3〜図5に示す。  
![kadai3-3](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai3-3.jpg)
<div align="center">
図３ 閾値96
</div>  

![kadai3-4](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai3-4.jpg)
<div align="center">
図４ 閾値128 
</div>  

![kadai3-5](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai3-5.jpg)
<div align="center">
図５ 閾値196
</div>  
