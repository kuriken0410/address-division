# Address separate program

A列に各規則性の無い住所データが入ったExcelをアパート・マンション名から2つに分けるプログラム。<br>
友人から上記の依頼を受けたため作成。<br>
友人のPCにPHP環境があったため、https://github.com/kuriken0410/phpspreadsheet/blob/main/address.php のプログラム内に必要事項を記入して使用します。<br>
また友人はPHPを含めプログラミングについて知識は無く、今後もプログラミングを学習することはありません。そんな状況の人でも使用できるプログラムとして作成しました。

改善点があればリクエスト欲しいです。

<br>

## 使用方法 
プログラムリンク：　https://github.com/kuriken0410/phpspreadsheet/blob/main/address.php

1．プログラム内のTODO EXのログファイルを設定して下さい。（こちらは一度設定すれば、今後変更する必要はありません。）

2．A列のみに住所データが入ったExcelを用意します。<br>
例： [住所分割テスト用.xlsx](https://github.com/kuriken0410/phpspreadsheet/files/10149315/default.xlsx)

3．プログラム内のTODO①〜④に必要事項を入力してターミナルで実行して下さい。

<br>

## 注意事項（問題点）
建物名が『55ビレッジ』や『５５小野ハウス』等のものは、『ビレッジ』や『小野ハウス』等の全角・半角数字の後から分割されてしまう。<br>
理由として、数字が続くと住所の号と建物名の境界線が区別不可のためです。<br>
この問題点に関してはプログラムの問題では無いと思いますが、念の為記載。<br>
<br>
例： 東京都新宿区新宿1-1-155ビレッジ101号室<br>
&emsp;⇒ 東京都新宿区新宿1-1-155 と ビレッジ101号室 に分割される。<br>
&emsp;⇒ 数字が続くと住所の号と、建物名の境界線が区別不可のため。 例：東京都新宿区新宿1-1-155ビレッジ101号室 ← 『1-1-1』、『1-1-15』、『1-1-155』の区別不可<br>
