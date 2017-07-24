# 課題9 レポート 

メディアンフィルターを適用し，ノイズ除去を行う.  
標準画像「ice」を原画像とする.この画像は縦480画素,横640画素の長方形のディジタルカラー画像である.  

まずは原画像を白黒濃淡画像に変換する.  

ORG=imread('Lenna.png'); % 原画像の入力  
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar;  

によって,白黒濃淡画像に変更された結果を図1に示す.  
![白黒濃淡画像](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai09/kadai09_00.jpg?raw=true)  
図1 白黒濃淡画像  

次に,ノイズの除去を行う前にノイズの載った画像を作成する.  

ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

その結果を図2に示す.  
![ノイズ添付](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai09/kadai09_01.jpg?raw=true)  
図2 ノイズ添付  

次に,平滑化フィルタでのノイズの除去を行う.  

IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

その結果を図3に示す.  
![平滑化フィルタ](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai09/kadai09_02.jpg?raw=true)  
図3 平滑化フィルタ  

次に,メディアンフィルタでのノイズの除去を行う.  

IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

その結果を図4に示す.  
![メディアンフィルタ](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai09/kadai09_03.jpg?raw=true)  
図4 メディアンフィルタ  

最後に,自らフィルタを設計し,適用,除去を行う.  

f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計  
IMG = filter2(f,IMG,'same'); % フィルタの適用  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

その結果を図5に示す.  
![フィルタの設計,適用](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai09/kadai09_04.jpg?raw=true)  
図5 フィルタの設計,適用  

各結果より,メディアンフィルタではほぼ元の画像に近いものが出力されているが,平滑化フィルタではノイズが残ったままの場所もある.自作フィルタではノイズは消えてはいるが,全体的に暗い仕上がりとなっていることがわかる.  
