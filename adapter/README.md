# Adapter (Wrapper)

## 概要

既存の実装を別の用途で使えるようにするもの

既存の実装がそのまま使えない場合に、既存の実装と必要なものの間のギャップを吸収することで、必要な形に変換する

- クラス（継承を使用）
- インスタンス（委譲を使用）

の２種類が存在


## クラス図

![Wikipediaより](https://upload.wikimedia.org/wikipedia/commons/e/e5/W3sDesign_Adapter_Design_Pattern_UML.jpg)

## 登場人物

### Target

必要なインターフェースの条件を定める

### Client

Targetのインターフェースを使用し何らかの処理を実行する

### Adaptee

Adaptされる側、既存の処理

### Adapter

Adapteeのメソッドを使用し、Targetで定められた条件を満たす

適応させる方法として、以下の二つが考えられる

- クラス（継承を使用）
- インスタンス（委譲を使用）

## メリット

既存の処理のに手を加えず再利用することができるため、既存のものに対するテストも必要なくなり、必要な処理を素早く作ることができる

既存の処理に対して、複数のインターフェースを用意し、そのインターフェース対して依存させることができる

例えば、Clientのversionごとに用意することで新規versionへの対応時も、既存の処理に手を加えずTargetとAdapterを作成するだけで済む