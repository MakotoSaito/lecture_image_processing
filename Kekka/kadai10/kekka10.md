# 課題10 レポート 

画像のエッジ抽出を行う.  
標準画像「ice」を原画像とする.この画像は縦480画素,横640画素の長方形のディジタルカラー画像である.  

ORG=imread('ice.jpg'); % 原画像の入力  
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar;  

によって,白黒濃淡画像に変更された結果を図1に示す.  
![白黒濃淡画像](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai10/kadai10_00.jpg?raw=true)  
図1 白黒濃淡画像  

次に,プレウィット法でのエッジ抽出を行う.  

IMG = edge(ORG,'prewitt'); % エッジ抽出（プレウィット法）  
imagesc(IMG); colormap('gray'); colorbar;% 画像表示  

その結果を図2に示す.  
![エッジ抽出（プレウィット法）](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai10/kadai10_01.jpg?raw=true)  
図2 エッジ抽出（プレウィット法）  

次に,ソベル法でのエッジ抽出を行う.  

IMG = edge(ORG,'sobel'); % エッジ抽出（ソベル法）  
imagesc(IMG); colormap('gray'); colorbar;% 画像表示  

その結果を図3に示す.  
![エッジ抽出（ソベル法）](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai10/kadai10_02.jpg?raw=true)  
図3 エッジ抽出（ソベル法）  

最後にキャニー法でのエッジ抽出を行う.  

IMG = edge(ORG,'canny'); % エッジ抽出（キャニー法）  
imagesc(IMG); colormap('gray'); colorbar;% 画像表示  

その結果を図4に示す.  
![エッジ抽出（キャニー法）](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai10/kadai10_03.jpg?raw=true)  
図4 エッジ抽出（キャニー法）  

結果より,プレウィット法とソベル法では非常に近いエッジが抽出できていることがわかり,ソベル法の方がわずかにだが抽出できている線が多い.キャニー法では抽出結果が独特なものとなっており,より細かく抽出できていることがわかる.  
