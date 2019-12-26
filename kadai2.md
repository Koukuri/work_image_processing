#課題２レポート

「flower」を原画像とする。この画像は縦512、横512画素による正方形のディジタルカラーである。

ORG=imread('flower.jpg'); % 原画像の入力
ORG = rgb2gray(ORG); colormap(gray); colorbar;
imagesc(ORG); axis image; % 画像の表示

より、原画像を読み込み、グレーカラーマップとして表示した結果を図１に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai2.1.png)
図１ 原画像のグレーカラーマップ

図１は256諧調なので2諧調にするには半分の128で分ければよい。

% ２階調画像の生成
IMG = ORG>128;\n
imagesc(IMG); colormap(gray); colorbar;  axis image;

2諧調画像の生成の結果を図２に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai2.2.png)
図２ 2諧調画像

同様に4諧調にするには64、128、192で分ける。

% ４階調画像の生成
IMG0 = ORG>64;
IMG1 = ORG>128;
IMG2 = ORG>192;
IMG = IMG0 + IMG1 + IMG2;
imagesc(IMG); colormap(gray); colorbar;  axis image;

4諧調画像の生成の結果を図３に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai2.3.png)
図３ 4諧調画像

同様に8諧調にするには32、64、96、128、160、192、224で分ける。

% ８階調画像の生成
IMG0 = ORG>32;
IMG1 = ORG>64;
IMG2 = ORG>96;
IMG3 = ORG>128;
IMG4 = ORG>160;
IMG5 = ORG>192;
IMG6 = ORG>224;
IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4 + IMG5 + IMG6;
imagesc(IMG); colormap(gray); colorbar;  axis image;

8諧調画像の生成の結果を図４に示す。

![原画像](https://github.com/Koukuri/work_image_processing/blob/master/image/kadai2.4.png)
図４ 8諧調画像
