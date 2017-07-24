# 課題8 レポート 

二値化された画像の連結成分にラベルを行う.  
標準画像「ice」を原画像とする.この画像は縦480画素,横640画素の長方形のディジタルカラー画像である.  

ORG=imread('Lenna.png'); % 原画像の入力  
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar;  

によって,白黒濃淡画像に変更された結果を図1に示す.  
![白黒濃淡画像](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai08/kadai08_00.jpg?raw=true)  
図1 白黒濃淡画像  


次に,閾値128で画像の二値化を行う. 

IMG = ORG > 128; % 閾値128で二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

その結果を図2に示す.  
![二値化](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai08/kadai08_01.jpg?raw=true)  
図2 二値化  

最後に,バイナリ イメージ内の連結要素をラベル付けを行う.  

IMG = bwlabeln(IMG); 
imagesc(IMG); colormap(jet); colorbar; % 画像の表示  
その結果を図3に示す.  
![連結要素のラベル付け](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai08/kadai08_02.jpg?raw=true)  
図3 連結要素のラベル付け  

出力結果より,同じ色彩を持つ場所が同じ色で表示されていることがわかる.  
