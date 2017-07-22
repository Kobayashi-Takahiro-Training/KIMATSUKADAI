# 課題3レポート   ###17EC039 小林崇寛

画像「chick」を原画として使用する.この画像は縦1066画素,横1600画素のディジタルカラー画像である.

ORG=imread('chick.png'); % 原画像の入力
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換
imagesc(ORG); colormap(gray); colorbar; % 画像の表示

により,原画の読み込み,白黒濃淡画像への変換,及び表示した結果を図1に示す.

![ひよこ](http://uploader.sakura.ne.jp/src/up162882.png?raw=true)  
<img src="http://uploader.sakura.ne.jp/src/up162882.png" alt="白黒ひよこ" title="ひよこ"width="76"height="102">
 図1　白黒濃淡色の原画像

白黒にした画像の輝度値が64に満たない画素を0（黒）,64以上の値を持つ画素を1（白）とするように処理する.このような処理において基準となる値を閾値,元の画像を白と黒だけの画像とする処理を2値化という.

IMG = ORG > 64; % 輝度値が64以上の画素を1，その他を0に変換
imagesc(IMG); colormap(gray); colorbar;

