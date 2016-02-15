# 概要 #
xstream-for-androidのソースを改変する場合など、Eclipseを使用したxstream-for-androidプロジェクトの設定方法

# プロジェクトの設定 #
  1. trunk/xstreamをJavaProjectとしてチェックアウト後、src/java, src/testをそれぞれソースプロジェクトとして設定
  1. ビルドパスにPureJavaではなく、android.jarを指定。さらに、lib/配下のjarもビルドパスに追加
# ビルド #
## Antを使用した場合 ##
下記は、xstream直下で実行する。
### コンパイル ###
```
ant compile
```
### テスト ###
```
ant test
```
### jar生成 ###
```
ant jar
```
## Mavenを使用した場合 ##
下記は、xstream直下で実行する。
### コンパイル ###
```
mvn compile
```
### テスト ###
```
mvn test
```
### jar生成 ###
```
mvn package
```
ただし、テストでエラーが発生する場合は、下記のコマンドでテストフェーズをスキップすることも可能。
```
mvn package -Dmaven.test.skip=true
```