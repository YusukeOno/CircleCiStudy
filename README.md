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

### CIをスキップしたい場合

コミットメッセージに ```[ci skip]``` または ```[skip ci]``` とキーワードを記述します。

### SSHデバッグしたい場合

CircleCIで実行されたジョブのコンテナーにSSHログインを行うことができます。これによりconfig.ymlを編集せず直接ターミナルから操作してコマンドの実行確認ができます。

SSh接続には、連携しているGitHubアカウントのSSHキーが必要です。

以下のコマンドでGitHubへのSSH接続確認を行えます。

```
$ ssh -T git@github.com
Hi YusukeOno! You've successfully authenticated, but GitHub does not provide shell access.
```

SSHデバッグを実行するとジョブはSSH接続待機状態となり、最後のステップが終わっても待機状態が維持されます。また、SSHログアウトしても、待機状態が維持されます。なので、ジョブをキャンセルして終了状態にする必要があります。

### 制約事項

ローカル環境にて実行することで、設定ファイルのチェックができますが、ワークフローの利用ができないため、単体ジョブの実行のみとなります。

## Reference Link

https://circleci.com/developer/orbs/orb/circleci/slack
