# 課題1 レポート

標準画像「ice」を原画像とする.この画像は縦480画素,横640画素の長方形のディジタルカラー画像である.  

ORG=imread('ice.jpg'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

によって,原画像を読み込み,カラー画像を白黒濃淡画像へ変換,表示した結果を図1に示す.  
![白黒濃淡画像](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai03/kadai3_0_noutan.jpg?waw=true)  
図1 白黒濃淡画像  


次は輝度値によって画素に処理を変える.  
はじめに,輝度値が64以上の画素を1，その他を0に変換とした処理を与える.  

IMG = ORG > 64; % 輝度値が64以上の画素を1，その他を0に変換
imagesc(IMG); colormap(gray); colorbar;  

その結果を図2に示す.  
![白黒濃淡画像 64](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai03/kadai3_64.jpg?waw=true)  
図2 白黒濃淡画像 64  


次に,輝度値が96以上の画素を1，その他を0に変換とした処理を与える.  

IMG = ORG > 96;  
imagesc(IMG); colormap(gray); colorbar;  

その結果を図3に示す.  
![白黒濃淡画像 96](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai03/kadai3_96.jpg?waw=true)  
図3 白黒濃淡画像 96  

次に,輝度値が128以上の画素を1，その他を0に変換とした処理を与える.  

IMG = ORG > 128;  
imagesc(IMG); colormap(gray); colorbar;  

その結果を図4に示す.  
![白黒濃淡画像 128](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai03/kadai3_128.jpg?waw=true)  
図4 白黒濃淡画像 128  

最後に,輝度値が192以上の画素を1，その他を0に変換とした処理を与える.  

IMG = ORG > 192;  
imagesc(IMG); colormap(gray); colorbar;  

その結果を図5に示す.  
![白黒濃淡画像 192](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai03/kadai3_192.jpg?waw=true)  
図5 白黒濃淡画像 192  

輝度値の閾値を高くすることによって,条件にかかる数値が多くなり,結果として画像が黒くなる画素が多くなることがわかる.  
