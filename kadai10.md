# 課題10

ORG=imread('images/cat2.jpg');  
ORG= rgb2gray(ORG);  
imagesc(ORG); colormap(gray); colorbar;  
pause;  

によって原画像を読み込み，グレースケールで表示した結果を図１に示す。  
![kadai10-1](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai10-1.jpg)
<div align="center">
図１ 原画像のグレースケール  
</div> 

IMG = edge(ORG,'prewitt');  
imagesc(IMG); colormap('gray'); colorbar;  

によってプレウィット法でエッジ抽出を行う。  
![kadai10-2](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai10-2.jpg)
<div align="center">
図２ エッジ抽出(プレウィット法)  
</div>

IMG = edge(ORG,'sobel');  
imagesc(IMG); colormap('gray'); colorbar;  

によってソベル法でエッジ抽出を行う。  
![kadai10-3](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai10-3.jpg)
<div align="center">
図３ エッジ抽出(ソベル法)  
</div>

IMG = edge(ORG,'canny');  
imagesc(IMG); colormap('gray'); colorbar;  

によってキャニー法でエッジ抽出を行う。  
![kadai10-4](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai10-4.jpg)
<div align="center">
図４ エッジ抽出(キャニー法)  
</div>
