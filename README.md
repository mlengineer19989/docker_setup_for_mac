# mac上でdocker desktopを使わないdocker環境構築手順を調査する

## Linux環境作成ツール候補
- lima:windowsのwsl2のようにmac上にLinux環境を構築する手法は様々あるが、limaがwsl2のやり方に最も近い印象。ファイル共有やポートフォーワーディングを自動で設定してくれて便利らしい。ただし、データ永続化やよく使うサブコマンドがないらしい。
(https://tech.mirrativ.stream/entry/2021/12/21/125127)
- Multipassが万能だという記事もある。
- とりあえず、limaが簡単そうなのでlimaで環境構築する。
- 参考サイト(https://qiita.com/kyosuke5_20/items/cd5f3df4e827c34d7c4a, https://qiita.com/hisato_imanishi/items/91d6881ff7c4d55b9ec4)
## lima+docker環境孤竹
- lima公式のGithubリポジトリ（https://github.com/lima-vm/lima/tree/15aba00bbb85e64c3e17ea3611b39b6503727064）






