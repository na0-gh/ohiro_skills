---
name: vue-best-practices
description: Vueのリアクティビティ/コンポーネント/パフォーマンス設計を整理する手順。実装品質を上げたい時に使用。
license: MIT
metadata:
  author: vinayakkulkarni, antfu
  source:
    - https://github.com/vinayakkulkarni/vue-nuxt-best-practices
    - https://github.com/antfu/skills
---
# Vue Best Practices

## いつ使うか
- Vueコンポーネントの設計指針を定めたい時
- リアクティビティの不具合や再レンダリングが気になる時
- Composition APIの使い方を整理したい時

## 参照ルール（最優先）
- `.cursor/rules/00-mindset.mdc`
- `.cursor/rules/27-testing-strategy.mdc`

## 実行手順
1. **目的整理**: 何を最適化するか（可読性/パフォーマンス/保守性）を明確化
2. **リアクティビティ整理**: `ref` / `reactive` / `toRefs` の使い分けを決める
3. **計算と副作用の分離**: `computed` は派生値、`watch` は副作用に限定
4. **テンプレ最適化**: `v-if`/`v-show`、`key` の使い方を統一
5. **パフォーマンス対策**: `v-once` / `v-memo` / 非同期コンポーネントを検討
6. **SSR配慮**: ブラウザ依存処理は ClientOnly で隔離

## チェックリスト
- destructuringでリアクティビティを壊していない
- `computed` が副作用を持っていない
- `watch` が過剰に深い監視になっていない
- `key` が安定している
- SSR/CSRで差分が出ない

## 出力テンプレ
1. 対象コンポーネント/画面
2. リアクティビティ設計方針
3. パフォーマンス方針
4. SSR配慮点
