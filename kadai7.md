# 課題７レポート

「flower」を原画像とする。この画像は縦512、横512画素による正方形のディジタルカラーである。

ORG = imread('flower.jpg'); % 画像の読み込み  
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

より、原画像を読み込み、白黒濃淡画像へ変換した結果を図１に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai7.1.png)
図１ 原画像の白黒濃淡画像

imhist(ORG); % 濃度ヒストグラムを生成、表示  

より生成した濃度ヒストグルムを図２に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai7.2.png)
図２ 濃度ヒストグルム

ORG = double(ORG);  
mn = min(ORG(:)); % 濃度値の最小値を算出  
mx = max(ORG(:)); % 濃度値の最大値を算出  
ORG = (ORG-mn)/(mx-mn)*255;  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

より、ダイナミックレンジを２５５にした結果を図３に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai7.3.png)
図３ ダイナミックレンジを２５５にした結果

ORG = uint8(ORG); % この行について考察せよ  
imhist(ORG); % 濃度ヒストグラムを生成、表示  

よりダイナミックレンジを２５５にした画像の濃度ヒストグルムを図４に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai7.4.png)
図４ 濃度ヒストグルム

図４よりダイナミックレンジが２５５になっていることがわかる。また、存在しない濃度が等間隔に表れていることがわかる。これは、ダイナミックレンジを拡大したからだと考えられる。また、図１と図３より、ダイナミックレンジを拡大しても、画像はほとんど変化しなかったことがわかる。
