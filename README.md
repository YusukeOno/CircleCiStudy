# CircleCiStudy
Studying is fun for me. CircleCI.

## Setup

https://github.com/CircleCI-Public/slack-orb/wiki/Setup

「Contexts」は、Circle CIのOrganization Settings>>Contextsにあります。

## Note

### ローカル環境での実行

https://circleci.com/docs/ja/2.0/local-cli/

### バリデーションチェック

```
$ circleci config validate -c [config.ymlへのファイルパス]
```

### 制約事項

ローカル環境にて実行することで、設定ファイルのチェックができますが、ワークフローの利用ができないため、単体ジョブの実行のみとなります。

## Reference Link

https://circleci.com/developer/orbs/orb/circleci/slack
