# 課題６レポート

「flower」を原画像とする。この画像は縦512、横512画素による正方形のディジタルカラーである。

ORG=imread('flower.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG);  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

より、原画像を読み込み、白黒濃淡画像へ変換した結果を図１に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai6.1.png)
図１ 原画像の白黒濃淡画像

IMG = ORG>128; % 128による二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

より、閾値を128として二値化した結果を図２に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai6.2.png)
図２ 閾値を128による二値化

IMG = dither(ORG); % ディザ法による二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

より、ディザ法による二値化した結果を図３に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai6.3.png)
図３ ディザ法による二値化

図２と図３より、128による二値化より、ディザ法による二値化のほうがより画像が鮮明であることがわかる。
