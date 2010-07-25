==========================
ligtran
==========================
---------------------------------------------------------------------------------------------
文字と文字をくっつけたり离隹したりすることでテキストを短くしたり長くするウェブサービス
---------------------------------------------------------------------------------------------

 :Homepage: http://ligtran.appspot.com

このウェブサイトについて
============================
これは文字と文字をくっつけたり離したりすることで、テキストを短くしたり長くするウェブサービスです。
 たとえば「バイドゥ株式会社」を長くすると「バイドゥ木朱式会ネ土」などとなります。
 使い方は下記のとおりです。

 #. 「短く」か「長く」を選びます。
 #. 一つ目の入力欄にテキストを入力します。
 #. 二つ目の欄に変換された結果が表示されます。

 変換の方法としては、標準的な合字の組([#]_, [#]_)と、その他の見た目に類似性のある文字列の組([#]_)とを用いています。

.. [#] `Unicode Normalization Forms`_
.. [#] `漢字構造情報データベース`_, `fonts.jp 漢字分解器`_
.. [#] 見た目の類似性による組は `不自然言語処理コンテスト`_ 応募時点では未実装

.. _Unicode Normalization Forms:
   http://unicode.org/reports/tr15/

.. _漢字構造情報データベース:
   http://www.kanji.zinbun.kyoto-u.ac.jp/projects/chise/ids/index.html.ja.iso-2022-jp

.. _fonts.jp 漢字分解器:
   http://www.fonts.jp/archives/search/

.. _不自然言語処理コンテスト:
   http://www.baidu.jp/unlp/

API
===============================
JSON形式でのAPIもあります。

例
  http://ligtran.appspot.com/ligature?str=fi を要求すると、 ::

     {"result": "\uFB01"}

  がかえってきます。
例
  http://ligtran.appspot.com/ligature/reverse?str=%E6%A0%AA を要求すると、 ::

     {"result": "\u30CD\u571F"}

  がかえってきます。

..  Local Variables: ***
..  mode: rst ***
..  tab-width: 5 ***
..  End: ***