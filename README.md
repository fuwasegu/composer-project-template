# fuwasegu/composer-project-template
Composer プロジェクトのテンプレートです．PHP8.1 以上を想定しています．
それ以下のバージョンに対応するパッケージを開発する場合は，それぞれの依存ライブラリのバージョンを調節してください．
このテンプレートには以下の 3 つの開発用ライブラリが含まれています
- php-cs-fixer (設定項目は yumemi-inc/php-cs-fixer-config を利用)
  - 自動フォーマッタ
- phpstan
  - 静的解析（型検査）ライブラリ
- phpunit
  - テストフレームワーク

また，Coveralls (https://coveralls.io/) を使う前提で，ci も完備しています
.github/workflows/ci.yml の on を適切に設定してください．

# .github/workflows/ci.yml で設定が必要な項目
## 必須
- on

## 任意
- jobs.build.strategy.matrix.php
  - 対応する PHP のバージョンに依る

# composer.json で設定が必要な項目
- name
- description
- authors
- keywords
- autoload のパス
- autoload-dev のパス