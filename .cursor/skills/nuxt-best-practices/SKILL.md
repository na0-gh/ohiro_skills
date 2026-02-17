---
name: nuxt-best-practices
description: Nuxtのデータ取得/SSR/サーバールート設計を整理する手順。安定した実装基盤を作る時に使用。
license: MIT
metadata:
  author: vinayakkulkarni, antfu
  source:
    - https://github.com/vinayakkulkarni/vue-nuxt-best-practices
    - https://github.com/antfu/skills
---
# Nuxt Best Practices

## いつ使うか
- Nuxtアプリの初期設計やリファクタリング
- `useFetch`/`useAsyncData` の運用方針を整理したい時
- SSR/SSGの整合性が不安な時

## 参照ルール（最優先）
- `.cursor/rules/23-security-policy.mdc`
- `.cursor/rules/27-testing-strategy.mdc`

## 実行手順
1. **レンダリング方針整理**: SSR/SSG/CSRの対象を分ける
2. **データ取得設計**: `useFetch`/`useAsyncData` のキー戦略を決める
3. **Runtime Config整備**: 公開/非公開の境界を明確化
4. **サーバールート設計**: 入力バリデーションとエラー設計を組み込む
5. **状態管理**: SSR安全な `useState` を前提に設計
6. **運用テスト**: 主要導線でSSR/CSR差分を確認

## チェックリスト
- データ取得キーが一意で安定
- Runtime Configの公開範囲が最小
- サーバールートに入力検証がある
- SSR/CSRで不整合が出ない

## 出力テンプレ
1. レンダリング方針
2. データ取得方針（useFetch/AsyncData）
3. サーバールート設計
4. SSRリスクと対策
