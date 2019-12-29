# 課題９レポート

「flower」を原画像とする。この画像は縦512、横512画素による正方形のディジタルカラーである。

ORG = imread('flower.jpg'); % 画像の読み込み  
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

より、原画像を読み込み、白黒濃淡画像へ変換した結果を図１に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai9.1.png)
図１ 原画像の白黒濃淡画像

ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

より、ノイズ添付した結果を図２に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai9.2.png)
図２　ノイズ添付

IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

より、平滑化フィルタで雑音除去した結果を図３に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai9.3.png)
図３ 平滑化フィルタで雑音除去

IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

より、メディアンフィルタで雑音除去した結果を図４に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai9.4.png)
図４ メディアンフィルタで雑音除去

f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計  
IMG = filter2(f,IMG,'same'); % フィルタの適用  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

より、設計したフィルタを適用した結果を図５に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai9.5.png)
図５ 設計したフィルタを適用

結果より、メディアンフィルタを用いるとノイズをきれいに除去できることが確認できる。
