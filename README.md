# ChatUI
Power Apps モデル駆動型アプリで動作する Chat UI のカスタムページです。 Copilot Studio で作成するエージェントではなく、AI Builder 及び Power Apps 、 PCF コントロールであえて構成されています。


## 概要
あえて Power Apps で作成することにより、チャット内にコピーのコントロールを配置したり、一部を拡大したり、プロンプトの提案を動的に出力させたりするような柔軟な画面上のカスタマイズを Power Apps の知識で行うことができます。

https://github.com/user-attachments/assets/61521ce0-87df-4521-802d-9a70380bc260

## 機能
```mermaid
graph TD
  A[Power Apps<br>モデル駆動型アプリ] --> B[Dataverse]
  B --> C[AI Chat テーブル<br>(会話履歴を保存)]
  A --> D[AI Builder コンポーネント]

  D --> E1[プロンプトの提案モデル]
  D --> E2[回答案の生成モデル]

  E1 --> C
  E2 --> C

  style A fill:#dff0d8,stroke:#333,stroke-width:1px
  style B fill:#d9edf7,stroke:#333,stroke-width:1px
  style C fill:#fcf8e3,stroke:#333,stroke-width:1px
  style D fill:#f2dede,stroke:#333,stroke-width:1px
  style E1 fill:#f5f5f5,stroke:#333,stroke-width:1px
  style E2 fill:#f5f5f5,stroke:#333,stroke-width:1px
```
* Power Apps モデル駆動型アプリ: アプリ UI を提供。
* AI Builder に接続される 2 種類のモデル：
*   プロンプトの提案モデル（ユーザー入力に応じた質問生成）
*   回答案の生成モデル（ユーザーの質問に対する回答生成）
* Chat テーブル は 会話履歴の保存 に使用される

## 前提条件

## インポート方法



