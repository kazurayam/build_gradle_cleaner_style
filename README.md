# build.gradleをDSLっぽくなくKotlinスクリプトトっぽくしかしGradleで書くには

## 解決したい問題

わたしはビルドシステム Gradle を多用している。ところで build.gradle ファイルの書き方として標準的に採用されているのはDSLっぽい書き方だ。

- [Groovyを知らない人のためのbuild.gradle読み書き入門](https://qiita.com/opengl-8080/items/a0bb31fb20cb6505188b)

標準的な書き方をわたしは好きでない。メソッド呼び出しなのか、プロパティへの値の代入なのか、見分けがつかない書き方だから、気持ちが悪いと感じる。

Groovy言語ではなくKotlin言語でbuild.gradle.ktsファイルを書くと、この気持ち悪さを回避できるようだ。

- [build.gradleをbuild.gradle.ktsへ移行したい！](https://qiita.com/niusounds/items/8def978f77a50df8735f)

ただし今までわたしはたくさんのプロジェクトのbuild.gradleをGroovyで作ってしまった。それをKotlineに書き換えるのはちょっとしんどい。Groovyインタープレタでビルドを実行するのは変わらないが、書き方をKotlinっぽく改めるに止める、のも一つの未知だと思う。では、具体的にどこをどう改めるのがいいんだろう？指針を明確にしたい。

