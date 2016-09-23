# GitHub Hands-on

## 環境の構築

### Gitのインストール

#### Mac

```
$ brew install git
```

#### Windows

https://git-for-windows.github.io/

### Rubyのインストール

#### Mac

```
$ brew install ruby
```

#### Windows

http://rubyinstaller.org/downloads/

`$PATH` に登録するのを忘れないこと。
https://www.evernote.com/l/ABWu6deGMHVDa78EJrVeRHcfGl91MeelL1QB/image.png

### Nodeのインストール

#### Mac

```
$ brew install node
```

#### Windows

https://nodejs.org/en/

### おまけ

もし `brew` で以下のようなエラーが出たら。。。

```
Error: You have not agreed to the Xcode license. Please resolve this by running:
  sudo xcodebuild -license
```

```
$ sudo xcodebuild -license
```

以下のように `~/.bash_profile` に書いておいて定期的にターミナルで `update` ってやるといいよ！

```
function update {
    set -ex

    npm update -g
    npm cache clean

    update_rubygems
    gem update bundler
    gem cleanup

    brew update
    brew upgrade
    brew cleanup

    echo "Update complete!!"
}
```

## Hands-on

HTML + JavaScriptのプロジェクトを作ってみる

1. GitHubでプロジェクトをつくる
2. GitHubにファイルをコミット
  1. `git clone`
  2. `git add`
  3. `git commit`
  4. `git push`
3. Issueをつかってみる
  1. Issueの投稿
  2. ラベル、マイルストーン
  3. コミットの際に特定のIssueに関連付け
4. Projectsを使って見る
5. 他社サービスとの連携
  1. Travis CI
