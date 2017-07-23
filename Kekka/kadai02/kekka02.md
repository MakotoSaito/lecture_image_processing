# 課題2 レポート


標準画像「ice」を原画像とする.この画像は縦480画素,横640画素の長方形のディジタルカラー画像である.  

ORG=imread('ice.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % 画像の表示  

によって,モノクロに処理,表示した結果を図1に示す.  
![モノクロ画像](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai02/kadai02_0gen.jpg?raw=true)  
図1 モノクロ画像  

画像を諧調で分けるには,画像の色データに対して閾値を持たせ,それにより処理を加えてやればよい.  
次は2諧調で表示したいため,画像に対し128という閾値を与えて処理している.  

IMG = ORG>128;  
imagesc(IMG); colormap(gray); colorbar; axis image;  

表示された結果を図2として示す.  
![2階調画像](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai02/kadai02_2dan.jpg?raw=true)  
図2 2階調画像  

同様に諧調を増やしたいならば,閾値を複数与えてやればよい.  
次は4諧調で表示したいため,同様に  

IMG0 = ORG>64;  
IMG1 = ORG>128;  
IMG2 = ORG>192;  
IMG = IMG0 + IMG1 + IMG2;  
imagesc(IMG); colormap(gray); colorbar; axis image;  

と閾値を増やす.表示された結果を図3として示す.  
![4階調画像](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai02/kadai02_4dan.jpg?raw=true)  
図3 4階調画像  

八階調でも同様であり,分けたい諧調の閾値を増やしてやればよい.  

IMG0=ORG>32;  
IMG1=ORG>64;  
IMG2=ORG>96;  
IMG3=ORG>128;  
IMG4=ORG>160;  
IMG5=ORG>192;  
IMG6=ORG>224;  
IMG=IMG0+IMG1+IMG2+IMG3+IMG4+IMG5+IMG6;  
imagesc(IMG); colormap(gray); colorbar; axis image;  

表示された結果を図3として示す.  
![4階調画像](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai02/kadai02_8dan.jpg?raw=true)  
図4 8階調画像  

このように,諧調が増えると色彩が増えることがわかる.