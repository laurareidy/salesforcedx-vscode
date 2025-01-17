---
title: Apex リファクタリング---

## リファクタリング: 名前変更

ソースで定義されている有効な Apex 記号はすべて名前を変更できます。この対象は、メソッド、ローカル、項目、プロパティ、コントラクタ、タイプ \(クラス、トリガ、列挙\) などです。名前変更を実行するには、名前を変更する記号を右クリックして、**[Rename Symbol \(シンボルの名前を変更\)]** を選択します。

![記号の名前変更プロセスを示す GIF](../../images/apex-rename-demo.gif)

名前変更を適用する前に、記号の名前が検証されます。検証に失敗すると、エラーメッセージに名前変更リファクタリングが適用されなかった理由が説明されます。検証に失敗するのは、新しい名前が有効な Apex 識別子でない場合や、時として新しい名前が既存の識別子名と競合する場合です\(これらの状況が容認される場合には、コンパイラエラーまたは実行時の動作に変更が生じる可能性があります\)。

![名前変更エラーを示す GIF](../../images/apex-rename-error.gif)

新しい名前が既存の識別子名と競合する場合は、競合が存在するコンテキストで、既存の名前への参照を完全修飾するよう試行されます。

![名前変更の競合を示す GIF](../../images/apex-rename-conflict.gif)

## リファクタリング: 定数の抽出

リテラルを定数に抽出できます。リテラルには、String、Integer、Long、Double、Decimal、Boolean などがあります。

1. エディタで、抽出する式を選択します。
1. 余白の電球をクリックして、[Extract Constant \(定数の抽出\)] を選択します。
1. リファクタリングが呼び出された場所から、新しい定数が、包含するクラスの項目として宣言されます。
1. これで、選択した式が新しい項目の名前に置換されます。

![定数の抽出を示す GIF](../../images/extract-constant.gif)

## リファクタリング: ローカル変数の抽出

式をローカル変数に抽出できます。

1. エディタで、抽出する式を選択します。
1. 余白の電球をクリックして、[Extract Variable \(変数の抽出\)] を選択します。
1. リファクタリングが呼び出された宣言の上の行に、新しいローカル定数が宣言されます。
1. これで、選択した式が新しいローカル変数の名前に置換されます。

![ローカル変数の抽出を示す GIF](../../images/extract-local-variable-other.gif)
