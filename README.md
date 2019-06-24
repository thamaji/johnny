johnny
====

プライベートリポジトリの go get とかするときにパスワードを入力できるようにするやつ


## Requirement

docker

### なんで docker が必要なの？

グローバルな git config で一時的に credential.helper を使いたい。
ホストの git config はその設定状況によっては使えないパターンがありそうなのと、ゴミが残るのを防ぐため、簡単に扱えるサンドボックス環境として docker を選んだ。このへんが解決できるなら docker である必要はない。

## Install

```
$ sudo curl -o /usr/local/bin/johnny -fSsL https://raw.githubusercontent.com/thamaji/johnny/master/johnny
$ sudo chmod +x /usr/local/bin/johnny
```

## Example

```
$ ./johnny dep init
Enter github username: yourname
Enter github password:
```
