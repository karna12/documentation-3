# リストの管理

リストはコンタクトを整理するための簡単な方法を提供します。これらのリストは様々なフィールドから構成することができます。

すべてのコンタクトのリストを表示すると、その特定のリストに一致するコンタクトの数を表示している右側の列に気づくかと思います。

![](http://drop.dbh.li/image/3v3F2v280n1z/Image%202014-11-16%20at%209.32.16%20PM.png)

### リストフィルタ

![List Filter](http://drop.dbh.li/image/3j350h370g0t/Image%202014-11-16%20at%209.13.39%20PM.png)

さらに、これらのフィルタは必要に応じて含めたり除外したりを組み合わせることができます。

![](http://drop.dbh.li/image/2u090o1n252V/Image%202014-11-16%20at%209.16.12%20PM.png)

フィールドを選択後、次に実行する操作の種類を選択することができます。この操作の種類はどのようにコンタクトをフィルタリングするかよって異なります。

![](http://drop.dbh.li/image/3o0a32313h07/Image%202014-11-16%20at%209.26.57%20PM.png)

### スマートリスト

リストを作成したら、cronジョブの実行により任意の適用可能なコンタクトが自動的に追加されます。これがスマートリストです。

スマートリストを最新に保つには、希望する間隔で次のコマンドを実行するcronジョブを作成します:

```
php /path/to/mautic/app/console mautic:segments:update --env=prod
```

このコマンドの実行により、フィルタに一致するコンタクトが追加され、一致しないコンタクトが削除されます。フィルターに関係なく、手動で追加されたコンタクトはリストにとどまります。

### 手動追加

スマートリストに加えて、リストボタンをクリックし、コンタクト詳細ビューのラジオボタンを選択することにより手動での追加も可能です。