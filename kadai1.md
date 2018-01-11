# 課題１
「Lenna」を原画像とする．この画像は縦1066画像，横1600画素による長方形のディジタルカラー画像である．    

ORG=imread('images/cat1.jpg'); % 原画像の入力  
imagesc(ORG); axis image; % 画像の表示    

によって，原画像を読み込み，表示した結果を図１に示す．

![cat1](https://github.com/y-ascll/image_processing/blob/master/images/cat1.jpg)
<div align="center">
図１ 原画像  
</div>  


原画像を1/2サンプリングするには，画像を1/2倍に縮小した後，2倍に拡大すればよい．なお，拡大する際には，単純補間するために「box」オプションを設定する．    

IMG = imresize(ORG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,2,'box'); % 画像の拡大    

1/2サンプリングの結果を図２に示す．
![kadai1-2](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai1-2.jpg)
<div align="center">
図２　1/2サンプリング  
</div>  


同様に原画像を1/4サンプリングするには，画像を1/2倍に縮小した後，2倍に拡大すればよい．すなわち，    

IMG = imresize(ORG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,2,'box'); % 画像の拡大    

とする．1/4サンプリングの結果を図３に示す.
![kadai1-3](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai1-3.jpg)
<div align="center">
図３　1/4サンプリング  
</div>  


1/8から1/32サンプリングは，    

IMG = imresize(ORG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,2,'box'); % 画像の拡大    

を繰り返す．サンプリングの結果を図４～６に示す．  

![kadai1-4](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai1-4.jpg)
<div align="center">
図４　1/8サンプリング  
</div>  


![kadai1-5](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai1-5.jpg)
<div align="center">
図５　1/16サンプリング  
</div>  


![kadai1-6](https://github.com/y-ascll/image_processing/blob/master/mdimages/kadai1-6.jpg)
<div align="center">
図６　1/32サンプリング  
</div>  


このようにサンプリング幅が大きくなると，モザイク状のサンプリング歪みが発生する．
