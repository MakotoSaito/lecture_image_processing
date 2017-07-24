# 課題7 レポート 

画素のダイナミックレンジを0から255とする.   
標準画像「ice」を原画像とする.この画像は縦480画素,横640画素の長方形のディジタルカラー画像である.  

ORG=imread('ice.jpg'); % 原画像の入力  
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar;  

によって,白黒濃淡画像に変更された結果を図1に示す.  
![白黒濃淡画像](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai07/kadai07_00.jpg?raw=true)  
図1 白黒濃淡画像  

次に,濃度ヒストグラムを出力する.  

imhist(ORG); % 濃度ヒストグラムを生成、表示  

によって出力された結果を図3に示す.  
![濃度ヒストグラム](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai07/kadai07_01.jpg?raw=true)  
図2 濃度ヒストグラム  

次に,画像のダイナミックレンジを0～255と定め,処理を行う.  

ORG = double(ORG);  
mn = min(ORG(:)); % 濃度値の最小値を算出  
mx = max(ORG(:)); % 濃度値の最大値を算出  
ORG = (ORG-mn)/(mx-mn)*255;  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

その結果を図3に示す.  
![ダイナミックレンジ0～255](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai07/kadai07_02.jpg?raw=true)  
図3 ダイナミックレンジ0～255

最後に,その濃度ヒストグラムを出力する.

ORG = uint8(ORG); % この行について考察せよ  
imhist(ORG); % 濃度ヒストグラムを生成、表示  

その結果を図4に示す.  
![ダイナミックレンジ0～255濃度ヒストグラム](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai07/kadai07_03.jpg?raw=true)  
図4 ダイナミックレンジ0～255濃度ヒストグラム

ORG = uint8(ORG)について  
二種類のヒストグラムを比較するとuint8を行ったヒストグラムでは縦のグラフ10本ごとに空白が挿入されていることがわかる.  


画像ではわかりづらいが,ダイナミックレンジの処理を行った後では右のグラフから0の数値が消えており,画像のデータサイズは29.8kバイトから29.1kバイトへと小さくなった.  
加えて画像の幅が少し短くなっている.  
