# DJYamabiko

物理演算ベースのボール転がしモバイルゲームプロジェクトです。
Unreal Engine 4 の Blueprint のみで実装されています。

## 概要

- **エンジン**: Unreal Engine 4.10
- **実装方法**: Blueprint のみ（C++ コードなし）
- **対象プラットフォーム**: モバイル（Android / 縦向き）
- **ゲームジャンル**: ボール転がし（物理演算）

## 必要環境

- [Unreal Engine 4.10](https://www.unrealengine.com/) (Epic Games Launcher からインストール可能)

## セットアップ

1. リポジトリをクローンします。

   ```bash
   git clone https://github.com/kotaoue/DJYamabiko.git
   ```

2. `DJYamabiko.uproject` をダブルクリックして Unreal Engine 4.10 で開きます。

3. エディタが起動したら、デフォルトマップ (`RollingBPExampleMap`) が自動的に開きます。

4. エディタ上部の **Play** ボタンを押してゲームを実行できます。

## ディレクトリ構成

```
DJYamabiko/
├── DJYamabiko.uproject       # Unreal プロジェクトファイル
├── Config/                   # エンジン・ゲーム設定ファイル
│   ├── DefaultEngine.ini     # エンジン設定（マップ、描画など）
│   ├── DefaultGame.ini       # ゲーム情報（プロジェクト名など）
│   └── DefaultInput.ini      # 入力設定（キー・タッチ）
└── Content/                  # ゲームコンテンツ
    ├── RollingBP/            # メインゲームコンテンツ
    │   ├── Blueprints/
    │   │   ├── PhysicsBallBP.uasset      # プレイヤーが操作するボール
    │   │   └── RollingGameMode.uasset    # ゲームモード
    │   └── Maps/
    │       └── RollingBPExampleMap.umap  # メインマップ
    ├── Rolling/              # ボール用マテリアル・メッシュ
    ├── Geometry/             # 基本ジオメトリアセット
    └── MobileStarterContent/ # Epic 提供のモバイル向けスターターコンテンツ
```

## 操作方法

| 操作 | PC | モバイル |
|------|-----|---------|
| 前後移動 | W / S キー、↑ / ↓ キー | 左バーチャルジョイスティック |
| 左右移動 | A / D キー、← / → キー | 左バーチャルジョイスティック |
| ジャンプ | スペースキー | タップ |

## 主要 Blueprint

| Blueprint | 概要 |
|-----------|------|
| `PhysicsBallBP` | 物理演算で動くプレイヤーボール。タッチ・キーボード入力を受け取り転がる。 |
| `RollingGameMode` | ゲームモード。ゲームの基本ルールを管理する。 |

## ライセンス

このプロジェクトには [Epic Games の MobileStarterContent](https://www.unrealengine.com/) が含まれています。
使用の際は Epic Games の EULA に従ってください。
