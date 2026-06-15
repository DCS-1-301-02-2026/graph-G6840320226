# 課題

## 課題 3.1 有向グラフ

![ex01.png](ex01.png)

プレビュー結果が上の図のようになるように，下記の記述を完成させよ．(接続関係が正しければ，上下が入れ替わっても構わない)

※ 日本語の文字列に対する箱の大きさが適切でない場合には，前後に空白を入れて調整せよ

```graphviz
digraph {
    rankdir = "LR";
    node [shape=box];


    "情報工学概論" -> "計算機工学";
    "計算機工学" -> "論理回路";

    "情報工学概論" -> "プログラミング基礎Ⅰ";
    "基礎ゼミ" -> "プログラミング基礎Ⅰ";
    "プログラミング基礎Ⅰ" -> "プログラミング基礎Ⅱ";

    "コンピュータリテラシー" -> "プログラミングⅠ";
    "プログラミングⅠ" -> "プログラミングⅡ";
}

```

## 課題 3.2 WBS

![ex02.png](ex02.png)

プレビュー結果が上の図のようになるように，下記の記述を完成させよ．(色や影などの違いは気にしなくてよい)

```plantUML
@startwbs ex02
* 拓殖大学
** 商学部
*** 経営学科
*** 国際ビジネス学科
*** 会計学科

** 政経学部
*** 法律政治学科
*** 経済学科

** 外国語学部
*** 英米語学科
*** 中国語学科
*** スペイン語学科
*** 国際日本学科

** 工学部
*** 機械システム工学科
*** 電子システム工学科
*** 情報工学科
*** デザイン学科

** 国際学部
*** 国際学科
@endwbs
```

## 課題 3.3 ユースケース図

![ex03.png](ex03.png)

プレビュー結果が上の図のようになるように，下記の記述を完成させよ．ただし，別名については適当に設定してよい．(色や影などの違いは気にしなくてよい)

```plantUML
@startuml ex03
left to right direction
actor "学生" as student
actor "教員" as teacher
rectangle "GitHub Classroom" {
  usecase "課題の登録" as uc8
  usecase "課題の受領" as uc7
  usecase "リポジトリのクローン" as uc6
  usecase "課題ファイルの修正" as uc5
  usecase "修正をステージに上げる" as uc4
  usecase "修正のコミット" as uc3
  usecase "リモートリポジトリにpush" as uc2
  usecase "提出結果の採点" as uc1
  }
student --> uc7
student --> uc6
student --> uc5
student --> uc4
student --> uc3
student --> uc2

teacher --> uc8
teacher --> uc1


@enduml
```

## 課題 3.4 オリジナルの図解

「有向グラフ」「WBS」「ユースケース図」のどれかを使って，
独自の図解を作成せよ．対象は自由に決めてよいが，
誰かのコピーにならないように留意せよ．

````graphviz
digraph {
    rankdir="LR";
    node [shape=box];

    "Idea" -> "Research";
    "Research" -> "Design";
    "Design" -> "Development";
    "Development" -> "Testing";
    "Testing" -> "Release";
}
```
```


## チェック
- [ ] 課題 3.1 有向グラフ
- [ ] 課題 3.2 WBS
- [ ] 課題 3.3 ユースケース図
- [ ] 課題 3.4 オリジナルの図解
