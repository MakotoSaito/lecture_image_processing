# 課題1 レポート

標準画像「ice」を原画像とする.この画像は縦480画素,横640画素の長方形のディジタルカラー画像である.  
ORG=imread('ice.jpg'); % 原画像の入力  
imagesc(ORG); axis image; % 画像の表示  

によって,原画像を読み込み,表示した結果を図1に示す.  
![原画像](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai01/kadai1_1.jpg?raw=true)  
図1 原画像　 

原画像を1/2サンプリングするには,画像を1/2倍に縮小した後,2倍に拡大すればよい.なお,拡大するには,単純保管をするために「box」オプションを設定する.  

IMG = imresize(ORG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,2,'box'); % 画像の拡大  

1/2サンプリングの結果を図２に示す．  
![原画像](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai01/kadai1_2.jpg?raw=true)  
図2 1/2サンプリング  
![原画像](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai01/kadai1_3.jpg?raw=true)  
![原画像](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai01/kadai1_4.jpg?raw=true)  
![原画像](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai01/kadai1_5.jpg?raw=true)  
![原画像](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai01/kadai1_6.jpg?raw=true)  
