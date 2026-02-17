---
name: pinia-state-management
description: Piniaのストア設計と運用ルールを整理する手順。状態管理をVue標準で統一したい時に使用。
license: MIT
metadata:
  author: antfu
  source: https://github.com/antfu/skills
---
# Pinia State Management

## いつ使うか
- Vue/Nuxtで状態管理をPiniaに統一する時
- ストア設計の責務や命名を整理したい時

## 参照ルール（最優先）
- `.cursor/rules/00-mindset.mdc`

## 実行手順
1. **領域分割**: ドメイン単位でストアを分ける
2. **責務定義**: state/actions/getters の責務を明確化
3. **SSR配慮**: 初期化とhydrationの流れを決める
4. **参照方法**: `storeToRefs` を使いリアクティビティを維持
5. **テスト設計**: actionsの副作用を分離して検証しやすくする

## チェックリスト
- gettersに副作用がない
- actionsが単一責務になっている
- ストアが肥大化していない
- SSR時に初期値が壊れていない

## 出力テンプレ
1. ストア一覧（ドメイン単位）
2. 主要state/actions/getters
3. SSR考慮点
4. テスト方針
