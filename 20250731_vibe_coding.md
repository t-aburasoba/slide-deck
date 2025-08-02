---
marp: true
title: "バイブコーディングでネイティブアプリを初めて作った話"
description: "1週間でネイティブアプリを作り、1か月でストア公開した体験談。Claude Codeを活用した開発プロセスとポイントを紹介"
url: "https://slides.ttsubasa.com/20250731_vibe_coding.html"
image: "https://slides.ttsubasa.com/20250731_vibe_coding.png"
author: "Ttsubasa"
theme: default
paginate: true
backgroundColor: #1a1a1a
color: #ccc
style: |
  section {
    font-family: 'Noto Sans JP', -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    font-size: 32px;
  }
  * {
    text-rendering: optimizeLegibility;
  }
  h1 {
    font-size: 80px;
    font-weight: 700;
  }
  h2 {
    font-size: 50px;
    font-weight: 500;
  }
  .subtitle {
    font-size: 30px;
    font-weight: 300;
  }
  strong, b {
    color: #4CAF50;
  }
  h1 strong, h1 b, h2 strong, h2 b {
    color: #4CAF50;
  }
  pre {
    background: #2d2d2d;
    border-radius: 8px;
    padding: 1.5em;
    margin: 1em 0;
    overflow-x: auto;
    box-shadow: 0 2px 8px rgba(0,0,0,0.3);
    text-align: left;
  }
  code {
    background: #2d2d2d;
    color: #f8f8f2;
    font-family: 'Fira Code', 'Monaco', 'Consolas', monospace;
  }
  pre code {
    background: transparent;
  }
---

# **バイブコーディング**で<br>**ネイティブアプリ**を<br>**初めて**作った話

---

# ネイティブアプリ<br>作ったこと**ありませんでした**

---

# **1週間ちょっと**で<br>動くものができた

---


# **1か月くらい**で<br>ストアに載せられた

---


# **初**登壇（LT）なのでお手柔らかに🙏

---

# デモ

<video controls width='1100' height="480">
  <source src="https://slide-deck-image.s3.ap-northeast-1.amazonaws.com/20250731_vibe_coding/app-demo.webm" type="video/webm">
</video>

---

# 自己紹介
## **Ttsubasa**
ソフトウェアエンジニア@GAOGAO
TypeScript（バックエンド/フロントエンド）
ベトナム（ホーチミン）に2年住んでました
英語勉強しています（TOEIC: 925）
Claude Code

---

# 伝えたいこと
## アプリ作るのは楽しい<br>バイブですぐ目に見える形にできる
※ グロースは抜き

---

# 話せないこと
## 実際の業務で使うために...
## Devin との比較...

---

# アジェンダ
## **何**を作ったか
## **どうやって**作ったか
## **バイブ**での私的ポイント

---

# **IELTS Diary**

英語日記支援アプリ

---

# 謝罪

## IELTS 勉強のアプリを作りました**が**
※ [IELTS](https://ieltsjp.com/japan/about)は英語の資格試験です

---

# 謝罪

## IELTS 受けたこと**ありません**<br>8/22に**初めて**受けます

---

# なぜ作った？

英語日記を書く勉強方法が**効果的**らしい

ChatGPTで添削しているが**記録が管理できない**

日記を書きながら勉強できるアプリが**欲しい**

---

# アプリの機能

📝 日記添削機能

📚 IELTS練習機能

🔥 Streak機能

💡 表現管理機能

---

# デモ

<video controls width='1100' height="480">
  <source src="https://slide-deck-image.s3.ap-northeast-1.amazonaws.com/20250731_vibe_coding/app-demo.webm" type="video/webm">
</video>

---

# 技術

**Flutter** - モバイルアプリ
**Cloud Functions** - バックエンド
**OpenAI API** - AI添削

データベースはこちらで持たない
認証もない
→ 個人情報観点でのリスクが少ないアプリ

---

# 開発時間

フルタイムで働いているので、**業務後の夜**
休みの日（お出かけしない日）

---

# 開発タイムライン
## Android

**4/25〜5/9** - 開発（約2週間）

**5/9** - クローズドテスト申請

**6/5** - オープンテスト版リリース

---

# リリースした時のSlack

![height:500px](https://slide-deck-image.s3.ap-northeast-1.amazonaws.com/20250731_vibe_coding/closed-release.png)

---

# リリースした時のSlack

![height:500px](https://slide-deck-image.s3.ap-northeast-1.amazonaws.com/20250731_vibe_coding/open-release.png)

---

# 開発タイムライン
## iOS

**6/19** - リリース

---


# リリースした時のSlack

![height:500px](https://slide-deck-image.s3.ap-northeast-1.amazonaws.com/20250731_vibe_coding/ios-release.png)

---

# つまり...

## 動くものは
## **1週間**とちょっとでできた

---

# つまり...

## ストアへ公開は
## **1か月**とちょっとでできた

---

# 開発の分担
## 1stリリースまで

環境構築：**自分**
相談役：**o3**
開発：**Cursor**
レビュー：**雰囲気**
デプロイ：**自分**

---

# 開発の分担
## 最近

相談役：**Claude Code (Opus 4)**
開発：**Claude Code (Opus 4 / Sonnet 4)**
レビュー：**Claude Code Actions**
デプロイ：**自分**

---

# 注意するポイント

いくつか進める中で注意点や
ポイントがあった

---

# ポイント①

## 全体設計は**頭のリソースを割いて**レビューする

---

## 全体設計

Cursor (Sonnet 4) の**最初の方針**
**直接** flutter から OpenAI API を叩く実装をしていた
flutter → OpenAI API

---

## 全体設計

Flutter に OpenAI の API Key を<br>**直接埋め込もう**とした

これヤバくない？

---

## 全体設計

**「これいいの？」「これやばくない？」**
の検知は人間の仕事

**別のAIにレビューさせる**でもいいですが、
闇雲に信頼するのは良くない

---

## 全体設計（o3に相談した）

API Keyは**バックエンド**で管理

**Cloud Functions**経由で呼び出し

**App Check**でセキュリティ強化

→ AIは実装だけでなく設計の相談相手

---

# ポイント②

## **CLAUDE.md**を日々、更新

何かClaudeが間違いを起こしたら、原因と再発防止策を検討させる
CLAUDE.md に端的に追記させる

不要なルールは削除

---

## CLAUDE.md

作業の進め方の定義

![](https://slide-deck-image.s3.ap-northeast-1.amazonaws.com/20250731_vibe_coding/claudemd-1.png)

---

## CLAUDE.md

ルールの明確化

![](https://slide-deck-image.s3.ap-northeast-1.amazonaws.com/20250731_vibe_coding/claudemd-2.png)

---

# ポイント③

## 破壊的操作をさせない
## **settings.json**

---

## Claude Code の行動を制限

![height:400px](https://slide-deck-image.s3.ap-northeast-1.amazonaws.com/20250731_vibe_coding/commte-setting.png)

https://x.com/commte/status/1936313902645887036

---

# ポイント④

## **静的解析**ツール

---

## 品質管理

**厳格な静的解析で開発効率を向上**

flutter_lints
dart_code_linter
Dart Code Metrics
husky

---

## 品質管理

**厳格な静的解析で開発効率を向上**

```
# .husky/pre-commit

dart format .
dart fix --apply
dcm check-unused-files lib
flutter test
flutter analyze --fatal-infos --fatal-warnings
```

---

# ポイント⑤
Commit メッセージを Claude に作成させる

[How I Use Claude Code](https://spiess.dev/blog/how-i-use-claude-code) 参考にした

```shell
#.zshrc

alias gcmauto="git commit -m \"\$(claude -p \"Look at the staged git changes and
create a summarizing git commit title. Only respond with the title and no affirmation.\")\""
```

---

# ポイント⑥

## **Claude Code GitHub Actions**

https://docs.anthropic.com/ja/docs/claude-code/github-actions

---

## 非同期で動くAIアシスタント

**デバッグログ**のリファクタ

**バグ**の調査

---

## スマホでIssue立てて
## メンションしたら
## **自動で調査**

---

## Issueをスマホで立ててメンション
電車でいじっていたらバグがあったのでGitHubにIssueを立ててメンション
![](https://slide-deck-image.s3.ap-northeast-1.amazonaws.com/20250731_vibe_coding/issue.png)

---

## Branchができて作業が完了していた
※ PR は自分で立てた
![height:500px](https://slide-deck-image.s3.ap-northeast-1.amazonaws.com/20250731_vibe_coding/pr.png)

---

## 仕事 / 移動中でも
## 裏で動いてくれる

---

# ポイント⑦
## Explore, plan, code, commit
[Claude Code: Best practices for agentic coding](https://www.anthropic.com/engineering/claude-code-best-practices)

① 関連ファイルを読ませる
② 計画を立てさせる（TODOに分割する）
③ TODOを進めさせる
④ Commitする

---

## 私の進め方 ①
まずは関連ファイルを読ませる
私が指定するというよりは探させている

![](https://slide-deck-image.s3.ap-northeast-1.amazonaws.com/20250731_vibe_coding/demo-1.png)

---

## 私の進め方 ②
やりたいこと（直したいこと）を説明し方針を調査
![](https://slide-deck-image.s3.ap-northeast-1.amazonaws.com/20250731_vibe_coding/demo-2.png)

---
## 私の進め方 ③
いい感じなのでTODOドキュメントにする
何ができて何ができてないのか把握するため

![](https://slide-deck-image.s3.ap-northeast-1.amazonaws.com/20250731_vibe_coding/demo-3.png)

---

## 私の進め方 ④

TODOを進めさせる
見積もり時間は謎w めちゃバッファ持ってくるw

![](https://slide-deck-image.s3.ap-northeast-1.amazonaws.com/20250731_vibe_coding/demo-4.png)

---

## 私の進め方⑤
若干きもいがいい感じ..! 
気に入らなければ再度作らせればいい

<video controls width='1100' height="480">
  <source src="https://slide-deck-image.s3.ap-northeast-1.amazonaws.com/20250731_vibe_coding/demo-result.webm" type="video/webm">
</video>

---

# まとめ

---

# 「何か**欲しい**！」と思ったら
# 作れる時代

---

## ただし...

**セキュリティ**は必ず検討
**設計**には人間の判断が必要
**品質管理**は必須

---

# ご清聴ありがとうございました！

バイブコーディングしていて全然IELTS勉強してないw

---

## 参考資料

[Claude Code: Best practices for agentic coding](https://www.anthropic.com/engineering/claude-code-best-practices)

[Claude Code に壊されないための denyルール完全ガイド](https://izanami.dev/post/d6f25eec-71aa-4746-8c0d-80c67a1459be)

[Claude Code どこまでも](https://speakerdeck.com/nwiizo/claude-everywhere)

[How I Use Claude Code](https://spiess.dev/blog/how-i-use-claude-code)