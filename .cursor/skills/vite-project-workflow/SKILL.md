---
name: vite-project-workflow
description: Viteの構成・ビルド・プラグイン選定を整理する手順。開発体験とビルド品質を安定させたい時に使用。
license: MIT
metadata:
  author: antfu
  source: https://github.com/antfu/skills
---
# Vite Project Workflow

## いつ使うか
- Viteプロジェクトの初期構成を決める時
- ビルド/最適化の方針を整理したい時

## 参照ルール（最優先）
- `.cursor/rules/00-mindset.mdc`

## 実行手順
1. **目的整理**: SPA/SSR/ライブラリのいずれかを明確化
2. **プラグイン選定**: 公式/定番の最小構成から始める
3. **エイリアス整理**: パス設計を早期に固定
4. **依存最適化**: `optimizeDeps` で初期起動を安定化
5. **ビルド方針**: 出力形式/分割/静的資産の扱いを定義

## チェックリスト
- 目的に合うビルド設定になっている
- 不要なプラグインが入っていない
- パス設計が統一されている

## 出力テンプレ
1. 用途（SPA/SSR/ライブラリ）
2. 採用プラグイン
3. 主要ビルド設定
4. 運用ルール
