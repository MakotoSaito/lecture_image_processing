# 課題5 レポート 

判別分析法を用いて画像二値化する.  
標準画像「ice」を原画像とする.この画像は縦480画素,横640画素の長方形のディジタルカラー画像である.  

ORG=imread('Lenna.png'); % 原画像の入力  
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar;  

によって,白黒濃淡画像に変更された結果を図1に示す.  
![白黒濃淡画像](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai05/kadia05_noutan.jpg?raw=true)  
図1 白黒濃淡画像  

その後,判別分析法を用いて画像の二値化を行う.  

H = imhist(ORG); %ヒストグラムのデータを列ベクトルEに格納  
myu_T = mean(H);  
max_val = 0;  
max_thres = 1;  
for i=1:255  
C1 = H(1:i); %ヒストグラムを2つのクラスに分ける  
C2 = H(i+1:256);  
n1 = sum(C1); %画素数の算出  
n2 = sum(C2);  
myu1 = mean(C1); %平均値の算出  
myu2 = mean(C2);  
sigma1 = var(C1); %分散の算出  
sigma2 = var(C2);  
sigma_w = (n1 *sigma1+n2*sigma2)/(n1+n2); %クラス内分散の算出  
sigma_B = (n1 *(myu1-myu_T)^2+n2*(myu2-myu_T)^2)/(n1+n2); %クラス間分散の算出  
if max_val<sigma_B/sigma_w  
max_val = sigma_B/sigma_w;  
max_thres =i;  
end;  
end;  

IMG = ORG > max_thres;
imagesc(IMG); colormap(gray); colorbar;

によって,二値化された画像を図2に示す  
![白黒濃淡画像二値化](https://github.com/MakotoSaito/lecture_image_processing/blob/master/Kekka/kadai05/kadai05_2chi.jpg?raw=true)  
図2 白黒濃淡画像二値化  

結果より,濃淡であった画像が白黒のみのになっていることがわかる.  
