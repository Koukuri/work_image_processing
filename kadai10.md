# 課題１０レポート

「flower」を原画像とする。この画像は縦512、横512画素による正方形のディジタルカラーである。

ORG = imread('flower.jpg'); % 原画像の入力  
ORG = rgb2gray(ORG); %カラーからグレイへの変換  
imagesc(ORG); colormap('gray'); colorbar;% 画像表示  

より、原画像を読み込み、白黒濃淡画像へ変換した結果を図１に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai10.1.png)
図１ 原画像の白黒濃淡画像

IMG = edge(ORG,'prewitt'); % エッジ抽出（プレウィット法）  
imagesc(IMG); colormap('gray'); colorbar;% 画像表示  

より、プレウィット法を用いてエッジ抽出した結果を図２に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai10.2.png)
図２ プレウィット法

IMG = edge(ORG,'sobel'); % エッジ抽出（ソベル法）  
imagesc(IMG); colormap('gray'); colorbar;% 画像表示  

より、ソベル法を用いてエッジ抽出した結果を図３に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai10.3.png)
図３ ソベル法

IMG = edge(ORG,'canny'); % エッジ抽出（キャニー法）  
imagesc(IMG); colormap('gray'); colorbar;% 画像表示  

より、キャニー法を用いてエッジ抽出した結果を図３に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai10.4.png)
図４キャニー法

プレウィット法とソベル法の結果の画像はほとんど同じであった。キャニー法は他の二つよりも多くのエッジを抽出していることがわかる。
