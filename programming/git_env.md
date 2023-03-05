# 概要

Git で SSH 接続利用する手順例を示します。

## 導入

Git、TortoiseGit、SSH鍵の作成、GitLabへの鍵の設定などは下記が詳しいです。

[TortoiseGitの導入とGitLabへの接続方法 - Qiita](https://qiita.com/SkyLaptor/items/6347f38c8c010f4d5bd2)

上記のリンクのうち、SSH 認証キー作成については下記参照。

```txt
> cd キーを作成する場所
> ssh-keygen.exe -t ed25519
```

- Git の改行コード自動変換機能は OFF にしましょう！
- 各種認証キーは　%USERPROFILE% に `.ssh` フォルダを作成して、その中に保存します。

## Git の知識

### 基礎知識

- [【絶対理解できる】Gitとは？特徴やできることまとめ！ | 侍エンジニアブログ](https://www.sejuku.net/blog/5756)
- [Microsoft の git 理解資料](https://docs.microsoft.com/ja-jp/learn/paths/intro-to-vc-git/)


|  用語  |  意味  |
| ---- | ---- |
|  リポジトリ  |  ファイルを格納する場所  |
|  ローカルリポジトリ  |  手元の PC にあるリポジトリ  |
|  リモートリポジトリ  |  チームで共有しているネットワーク上のリポジトリ  |
|  コミット  |  ローカルリポジトリに修正ファイルを入れること  |
|  プッシュ  |  ローカルリポジトリにコミットしたファイルをリモートリポジトリに押し込むこと  |
|  プル  |  リモートリポジトリの最新をローカルリポジトリに引き出すこと  |
|  リビジョン  |  コミットした単位。複数のファイルを含めることができる  |
|  ブランチ  |  修正の履歴を管理する枝。この枝を分けると、同じファイル一式を別の方向に進化させることができる  |


### その他

- コマンドは覚えたほうがよいが、基本的に TortoiseGit とか、Android Studio／Visual Studio／Visual Studio Code などのような GUI から操作するので、覚えなくても困らない。
