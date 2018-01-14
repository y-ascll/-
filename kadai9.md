# 課題9

ORG=imread('images/cat2.jpg');  
ORG= rgb2gray(ORG);  
imagesc(ORG); colormap(gray); colorbar;  
pause;  

によって原画像を読み込み，グレースケールで表示した結果を図１に示す。  
![kadai9-1](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai9-1.jpg)
<div align="center">
図１ 原画像のグレースケール  
</div> 

ORG = imnoise(ORG,'salt & pepper',0.02);  
imagesc(ORG); colormap(gray); colorbar;  

によってノイズを添付する。  
![kadai9-2](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai9-2.jpg)
<div align="center">
図２ ノイズ添付後  
</div> 

IMG = filter2(fspecial('average',3),ORG);  
imagesc(IMG); colormap(gray); colorbar;  

によって平滑化フィルタでノイズを除去する。  
![kadai9-3](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai9-3.jpg)
<div align="center">
図３ 平滑化フィルタ適用後  
</div> 

IMG = medfilt2(ORG,[3 3]);  
imagesc(IMG); colormap(gray); colorbar;  

によってメディアンフィルタでノイズを除去する。  
![kadai9-4](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai9-4.jpg)
<div align="center">
図４ メディアンフィルタ適用後  
</div> 

f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計  
IMG = filter2(f,IMG,'same'); % フィルタの適用  
imagesc(IMG); colormap(gray); colorbar;  

によってフィルタを設定し表示すると以下のようになる。  
![kadai9-5](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai9-5.jpg)
<div align="center">
図５ 設計フィルタ適用後  
</div> 
