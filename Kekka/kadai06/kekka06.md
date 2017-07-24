# 課題6 レポート 

標準画像「ice」を原画像とする.この画像は縦480画素,横640画素の長方形のディジタルカラー画像である.  
画像の

ORG=imread('Lenna.png'); % 原画像の入力  
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar;  

によって,白黒濃淡画像に変更された結果を図1に示す.  
![白黒濃淡画像](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai06/kadai06_00.jpg?raw=true)  
図1 白黒濃淡画像  


次に,閾値を128としての二値化を行う. 

IMG = ORG>128; % 128による二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  
pause;  

によって,二値化された結果を図2に示す.  
![閾値による二値化](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai06/kadai06_01.jpg?raw=true)  
図2 閾値による二値化  

最後に,ディザ法による二値化を行う.  

IMG = dither(ORG); % ディザ法による二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

によって,二値化された結果を図3に示す.  
![ディザ法による二値化](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai06/kadai06_02.jpg?raw=true)  
図3 ディザ法による二値化  

出力結果より,閾値による二値化ではきれいに出力できているのに対し,ディザ法では線上のノイズのようなものが走っていることがわかる.  
