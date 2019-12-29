# 課題４レポート

「flower」を原画像とする。この画像は縦512、横512画素による正方形のディジタルカラーである。

ORG=imread('flower.jpg'); % 原画像の入力  
ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar;

より、原画像を読み込み、白黒濃淡画像へ変換した結果を図１に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai4.1.png)
図１ 原画像の白黒濃淡画像

imhist(ORG); % ヒストグラムの表示  

より、画像の濃度ヒストグラムを生成した結果を図２に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai4.2.png)
図２ 「flower」の濃度ヒストグラム

図２よりヒストグラムには山となる部分と谷になっている部分があることがわかる。
また、濃度値がとても小さいところと大きいところに使われていない濃度領域があることが確認できる。
