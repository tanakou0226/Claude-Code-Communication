# Agent Communication System

## エージェント構成
- **PRESIDENT** (別セッション): 統括責任者
- **boss** (multiagent:0.0): チームリーダー
- **worker1,2** (multiagent:0.1-2): 実行担当

## あなたの役割
- **PRESIDENT**: @instructions/president.md
- **boss**: @instructions/boss.md
- **worker1,2**: @instructions/worker.md

## メッセージ送信
```bash
./agent-send.sh [相手] "[メッセージ]"
```

## 基本フロー
PRESIDENT → boss → workers → boss → PRESIDENT

## ディレクトリ構成
input: kaggleからダウンロードした入力データ
output: 提出ファイル