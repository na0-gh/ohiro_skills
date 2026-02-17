---
name: pnpm-workflow
description: pnpmのワークスペース運用と依存管理を整理する手順。モノレポや依存管理を安定させたい時に使用。
license: MIT
metadata:
  author: antfu
  source: https://github.com/antfu/skills
---
# pnpm Workflow

## いつ使うか
- pnpmでモノレポ運用を始める時
- 依存解決やスクリプト運用を標準化したい時

## 実行手順
1. **ワークスペース定義**: `pnpm-workspace.yaml` を整理
2. **依存方針**: 共有/局所依存の境界を決める
3. **フィルタ運用**: `-F` の運用ルールを決める
4. **ロック管理**: lockfile更新の手順を明確化
5. **CI設計**: キャッシュ/インストール手順を固定化

## チェックリスト
- 依存の重複が最小化されている
- スクリプトの実行範囲が明確
- lockfileの更新ルールが統一されている

## 出力テンプレ
1. ワークスペース構成
2. 依存管理方針
3. フィルタ運用ルール
4. CI運用
