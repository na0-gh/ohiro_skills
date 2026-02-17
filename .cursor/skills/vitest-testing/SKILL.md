---
name: vitest-testing
description: Vitestを使った単体テスト設計と運用手順。フロントの品質担保を強化したい時に使用。
license: MIT
metadata:
  author: antfu
  source: https://github.com/antfu/skills
---
# Vitest Testing

## いつ使うか
- Vue/Vite環境で単体テストを整備したい時
- CIでテスト品質を安定させたい時

## 参照ルール（最優先）
- `.cursor/rules/27-testing-strategy.mdc`

## 実行手順
1. **テスト範囲定義**: 重要ロジック/コンポーネントを優先
2. **設定整理**: `setupFiles` / `environment` を明確化
3. **テスト設計**: 1テスト=1目的、境界ケースを先に書く
4. **モック方針**: 外部依存は最小限にモック
5. **CI運用**: `--runInBand` など安定運用のフラグを決める

## チェックリスト
- flakyなテストがない
- 実行時間が許容範囲
- テスト失敗時の原因が追いやすい

## 出力テンプレ
1. 対象範囲
2. テスト構成
3. モック方針
4. CI運用
