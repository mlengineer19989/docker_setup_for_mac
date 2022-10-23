# mac上でdocker desktopを使わないdocker環境構築手順を調査する

## Linux環境作成ツール候補
- lima:windowsのwsl2のようにmac上にLinux環境を構築する手法は様々あるが、limaがwsl2のやり方に最も近い印象。ファイル共有やポートフォーワーディングを自動で設定してくれて便利らしい。ただし、データ永続化やよく使うサブコマンドがないらしい。
(https://tech.mirrativ.stream/entry/2021/12/21/125127)
- Multipassが万能だという記事もある。
- とりあえず、limaが簡単そうなのでlimaで環境構築する。
- 参考サイト(https://qiita.com/kyosuke5_20/items/cd5f3df4e827c34d7c4a, https://qiita.com/hisato_imanishi/items/91d6881ff7c4d55b9ec4)
## lima+docker環境孤竹
- lima公式のGithubリポジトリ（https://github.com/lima-vm/lima/tree/15aba00bbb85e64c3e17ea3611b39b6503727064）

- 参考サイト（https://korosuke613.hatenablog.com/entry/2021/09/18/docker-on-lima）

1. limaをインストール
> brew install lima

2. limaの設定ファイルexample/docker.yamlを作成(https://github.com/lima-vm/lima/blob/15aba00bbb85e64c3e17ea3611b39b6503727064/examples/docker.yaml)

3. docker.yamlのあるディレクトリで以下のコマンドを実行
> limactl start docker

ただし、以下のエラーが出た場合は、サイト（https://zenn.dev/kit_ok/articles/8a0e3d264756e0）
を参照。
>FATA[00xx] exiting, status={Running:false Degraded:false Exiting:true Errors:[] SSHLocalPort:0} (hint: see "/Users/xxx/.lima/xxx/ha.stderr.log")


