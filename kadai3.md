# 課題３レポート

「flower」を原画像とする。この画像は縦512、横512画素による正方形のディジタルカラーである。

ORG=imread('flower.jpg'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示

より、原画像を読み込み、白黒濃淡画像へ変換した結果を図１に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai3.1.png)
図１ 原画像の白黒濃淡画像

IMG = ORG > 64; % 輝度値が64以上の画素を1，その他を0に変換  
imagesc(IMG); colormap(gray); colorbar;

より、閾値を64としたときの閾値処理した画像を図２に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai3.2.png)
図２ 閾値を64としたときの閾値処理

同様に閾値を96、128、192とした時の閾値処理を図３～５に示す。

IMG = ORG > 96;  
imagesc(IMG); colormap(gray); colorbar;

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai3.3.png)
図３ 閾値を96としたときの閾値処理

IMG = ORG > 128;  
imagesc(IMG); colormap(gray); colorbar;

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai3.4.png)
図４ 閾値を128としたときの閾値処理

IMG = ORG > 192;  
imagesc(IMG); colormap(gray); colorbar;

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai3.5.png)
図５ 閾値を192としたときの閾値処理

閾値が小さい値のときの閾値処理をすると画像は白い部分が多くなり、大きい値の時は画像は黒い部分が多くなる。
