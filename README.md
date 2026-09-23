# 進化計算コンペ2026

交叉・突然変異の後に、選択されたコントロール数が制約範囲の6～12件を外れた場合、ランダムに候補を追加または削除して範囲内に戻す処理をga.hのプログラムに追加した。
ファイル構成は以下。

## ファイル構成

```
orienteering-cpp-test/
├── const.h            # 共通定数（コントロール数の制約・目標値・GAパラメータ等）
├── csv_loader.h/cpp   # CSV ロード（landmarks/nodes/edges）
├── graph.h/cpp        # 道路ネットワーク + Dijkstra + 経路キャッシュ
├── evaluate.h/cpp     # 染色体デコード + 4目的関数 + 評価関数
├── ga.h/cpp           # GA 操作（選択・交叉・突然変異・メインループ）
├── main.cpp           # エントリポイント・入出力
├── Makefile           # ビルド設定（コマンドラインから make で利用）
├── input/             # 入力 CSV ファイル
│   ├── landmarks.csv
│   ├── nodes.csv
│   ├── edges.csv
│   └── seimon.csv
├── output/            # 実行結果出力先
│   ├── best_course.json
│   └── fitness_history.csv
└── README.md
```
