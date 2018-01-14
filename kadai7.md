# 課題7

ORG=imread('images/cat1.jpg');  
ORG= rgb2gray(ORG);  
imagesc(ORG); colormap(gray); colorbar;  
pause;  

によって原画像を読み込み，グレースケールで表示した結果を図１に示す。  

![kadai7-1](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai7-1.jpg)
<div align="center">
図１ 原画像のグレースケール  
</div> 

imhist(ORG);  

によって濃度ヒストグラムを生成し次のように表示された。  
![kadai7-2](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai7-2.jpg)
<div align="center">
図２ 濃度ヒストグラム  
</div> 

ORG = double(ORG);  
mn = min(ORG(:));  
mx = max(ORG(:));  
ORG = (ORG-mn)/(mx-mn)*255;  
imagesc(ORG); colormap(gray); colorbar;  

ORG = uint8(ORG);  
imhist(ORG);  　　

によってダイナミックレンジを255まで拡大し符号なし整数でヒストグラム表示している。

![kadai7-3](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai7-3.jpg)
<div align="center">
図３ ダイナミックレンジ拡大後の画像  
</div> 

![kadai7-4](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai7-4.jpg)
<div align="center">
図４ ダイナミックレンジ拡大後のヒストグラム 
</div> 

図１と図３を比較するとダイナミックレンジが拡大されたため若干画像が明るくなったように見える。また，図４のヒストグラムではところどころ成分がなくなっているが，これはdouble型で計算したものをunit8で整数型に丸めたために発生したものだと考えられる。
