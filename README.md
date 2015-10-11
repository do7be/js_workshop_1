# js workshop #1

## 概要

### 日時

2015/10/15 19:30〜20:30

### 目的

Nodeのインストール。および実際に触ってみてもらうことで、簡単に実行できることや、実装のおもしろさを感じてもらう。

### 想定参加者

* JavaScriptの基本文法を理解している
  * console.log()
  * var hoge


### 内容

* git clone
* Node導入
* console.logを実行してみる
* Socket.ioのchatにアクセス
* Socket.ioのchatを動かしてみる
* learnyounode


### 持ち物

ノートPC

* Mac推奨
* WinでもいいがVM構築必須
* Git環境


## workshop本題

### 準備

#### ワークショップ用リポジトリをクローンする

```
$ cd ${適当なディレクトリ}
$ git clone https://github.com/do7be/js_workshop_1.git
$ cd js_workshop_1
```


### Node導入

#### nodebrewインストール(Nodeのバージョン管理用)

```
$ curl -L git.io/nodebrew | perl - setup
~/.bash_profile に以下を追加します。

export PATH=$HOME/.nodebrew/current/bin:$PATH
$ source ~/.bash_profile
$ nodebrew -v
nodebrew 0.8.1
```

#### Nodeインストール

```
$ nodebrew install-binary v4.1.2
```

#### Nodeのバージョン切り替え

nodebrewで入れた場合は、バージョン切り替えを行うことでどのバージョンのNodeを使用するか選択することができる。

```
$ nodebrew ls
v4.1.2

current: none

$ nodebrew use v4.1.2
use v4.1.2

$ node -v
v4.1.2

$ npm -v
3.3.6

```

#### （備考）単語説明

* Node：Node.js本体
* nodebrew：Node.jsのバージョン管理システム
* NPM：Nodeのパッケージ管理システム


### console.logを実行してみる

```
$ vi index.js
console.log('Hello Node.js!');

$ node index.js
```


### Socket.ioのchatにアクセス

いろいろいじってみる

http://socket.io/demos/chat/



### Socket.ioのchatを動かしてみる

```
$ cd ./examples/chat/
$ npm install
$ node ./index.js
```

http://localhost:3000/


### （時間が余ったら）learnyounode

Node.js入門者用workshopper

http://nodeschool.io/

```
$ npm install -g learnyounode
$ cd ${適当なディレクトリ}
$ learnyounode
```

## LICENSE

Thanks to https://github.com/socketio/socket.io