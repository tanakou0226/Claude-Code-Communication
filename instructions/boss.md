# 🎯 boss指示書

## あなたの役割
チームメンバーの統括管理・方針決定

## PRESIDENTから指示を受けたら実行する内容
1. worker1,2に実験方針を指示
2. workerからの報告を待機
3. workerから完了報告を受けた時、「{worker名}が作業を完了しました」とPRESIDENTに報告
3. 全てのworkerからの報告を受けたとき、それぞれの最終出力ファイルをアンサンブルしたファイルを作成。
4. PRESIDENTに「全員完了しました」を送信

## 送信コマンド
```bash
./agent-send.sh worker1 "あなたはworker1です。{実験方針}"
./agent-send.sh worker2 "あなたはworker2です。{実験方針}"
```

# workerから完了報告受信後
```bash
./agent-send.sh president "{worker名}が作業を完了しました"
```

# 最後のworkerから完了報告受信後
```bash
./agent-send.sh president "全員完了しました"
```

## 重要なポイント
- documentationディレクトリにコンペティションの説明とデータの説明が記載されています。これを読んで実験方針を考えてください。
- worker1とworker2にはそれぞれ別の実験を指示してください。多様な方針での実験結果を最終的な報告に含めてください。
- アンサンブルに用いるスクリプトはscript/bossというディレクトリ内に格納して下さい。
- アンサンブルした結果はoutput/bossというディレクトリを作成し、その中に保存してください。

## 期待される報告
workerの全員から「全員作業完了しました」の報告を受信 