# 課題4 レポート

標準画像「ice」を原画像とする.この画像は縦480画素,横640画素の長方形のディジタルカラー画像である.  
原画像をもちいて,画素の濃度ヒストグラムを作成する.  

ORG=imread('Lenna.png'); % 原画像の入力  
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar;  

によって,白黒濃淡画像に変更された結果を図1に示す.  
によって,白黒濃淡画像に変更された画像のヒストグラムの結果を図1に示す.  
![白黒濃淡画像](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai04/kadai04_noutan.jpg?waw=true)  
図1 白黒濃淡画像  

その後,その画像のヒストグラムを表示する.

imhist(ORG); % ヒストグラムの表示  

その結果を図2に示す.  

![白黒濃淡画像ヒストグラム](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai04/kadai04_noutan_hist.jpg?waw=true)  
図1 白黒濃淡画像ヒストグラム  

原画像を白黒濃淡画像に変更した後,ヒストグラムとして出力されたことがわかる.  
