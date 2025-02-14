# 内部リンク自動挿入システム

## 概要
このリポジトリは、GitHub Actions と独自スクリプト（例：Python）を活用し、WordPress の投稿本文に対して自動で内部リンクを挿入する仕組みを実装するためのサンプルプロジェクトです。本システムでは、以下の機能を実現します。

- **自動リンク挿入ロジック**  
  投稿本文内の指定キーワードに対して、事前に定義したリンク先 URL を挿入します。  
  ※1記事あたりのリンク挿入数や、既存リンクの除外など、細かい制御が可能です。

- **WordPress 連携**  
  WP REST API や WP-CLI＋SSH を利用して、対象の投稿を取得・更新します。  
  認証情報は GitHub Actions の Secrets で安全に管理します。

- **GitHub Actions による自動化**  
  手動実行、スケジュール実行、プッシュ時など任意のトリガーでスクリプトを実行します。

- **バージョン管理**  
  投稿本文やリンク設定ファイルを GitHub 上で管理し、変更履歴を追跡可能にします。

## フォルダ構成
以下はリポジトリの基本的なフォルダ構成例です。

