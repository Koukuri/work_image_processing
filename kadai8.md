# 課題８レポート

「flower」を原画像とする。この画像は縦512、横512画素による正方形のディジタルカラーである。

ORG = imread('flower.jpg'); % 画像の読み込み  
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

より、原画像を読み込み、白黒濃淡画像へ変換した結果を図１に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai8.1.png)
図１ 原画像の白黒濃淡画像

IMG = ORG > 128; % 閾値128で二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示　　

より、閾値128で二値化した結果を図２に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai8.2.png)
図２ 閾値128で二値化

IMG = bwlabeln(IMG);  
imagesc(IMG); colormap(jet); colorbar; % 画像の表示　　

より、画像の連結成分をラベル付けした結果を図３に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai8.3.png)
図３ 連結成分をラベル付け

図３より、それぞれの連結成分に色が振り分けられていることがわかる。
