---
title: "Vim 100 [Day 1] skkeletonを使ってみる"
emoji: "🔥"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["vim", "neovim"]
published: true
---

## はじめに

Vim について何かを書きたいと思いました。

Vim を初めて知ったのは十数年も前になりますが、
正直なところ、まだまだ基本しかわかりません。

なので書くことにより、もっと Vim に詳しくなればと思い、
とりあえず 100 日を目標にしました。

## 1 日目でやったこと

Vim について書くので、やはり Vim を使わなきゃ、
と思っちゃいました。

なので、初日は Vim からでも日本語を入力できるようにしました。
具体的には、「skkeleton」というプラグインを入れてみました。

漢字に変換する場合、最初のローマ字を大文字にするという
独特なルールがありますが、とにかく静かで気持ちいいです。

## skkeleton のインストール

導入の手順はこちらの記事を参考にさせていただきました。

https://zenn.dev/kuu/articles/vac2021-skkeleton

最初は何故かうまくいきませんでした。
それで、いったんほかのプラグインを全部アンインストールしてみたら、
正しく動きました。

現状の設定ファイルは以下のとおりです。

```vim: ~/.config/nvim/init.vim
call plug#begin('~/.vim/plugged')
Plug 'vim-denops/denops.vim'
Plug 'vim-skk/skkeleton'
call plug#end()

" skkeleton
call skkeleton#config({ 'globalJisyo': '~/.skk/SKK-JISYO.L' })
imap <C-j> <Plug>(skkeleton-enable)
cmap <C-j> <Plug>(skkeleton-enable)
```

skkeleton 以外は何も入っていないので、初日の気分にぴったりです。

## skkeleton の使い方

skkeleton の使い方は上の記事にも書かれましたので、そちらを参考にすればよいと思います。

ただ、カタカナの入力方法に触れていなかったようです。

それで自分で調べてわかりました。

`<q>` を打つことで、ひらがな／カタカナの切り替えができます。


## Day 1 のまとめ

Vim で日本語を入力するために、いったん設定ファイルの内容をすっきりしましたので、
明日から少しずつ戻していこうと思います。






