# 第２回　講座/課題で学んだこと 

## GitとCloud9の連携方法

#### Cloud9においてSSHキーを発行し、GitHubに登録

1. ターミナル上でcd ~/.ssh (.sshディレクトリに移動)
2. ssh-keygen（SSHキーの作成)
3. cat ~/.ssh/id_rsa.pub (キーの表示)　※コピーしておく
4. GitHub画面右上の settings > SSH and GPG keys > New SSH keys > Titleは自由 　Keyはコピーした分をペースト　入力が完了したら　  Add SSH Keyをクリック
5. 再度ターミナルに戻り ssh -T git@github.com　と入力し連携が完了

## 新規リポジトリの作成から変更内容のプッシュまで
1.  GitHub画面右上の＋ボタンからNew repository　で新規リポジトリの作成
2.  ターミナル上　git init で .gitフォルダを作成（この中に新規リポジトリをクローンする）
3. git clone https://~ （新規作成したリポジトリのCode > Clone HTTPS の項目をコピー&ペースト）
4. git branch lecture02 （lecture02ブランチを作成）
5. git checkout lecture02 （作成したlecture02ブランチへ移動）
6. lecture02.md ファイルを作成
7. git add lecture02
8. git commit -m "〇〇"　（コメントを入れて変更内容をコミット）
9. git push origin lecture02  (作成した内容をリモートリポジトリへプッシュ) 


## Gitの設定（PCにGitをダウンロードした時点で設定可能）

- git config コマンドを使用する
- 種別は　-system(システム全体) 、-global(該当ユーザーの全リポジトリ)、 -local(該当のリポジトリのみ)がある
- git config --global init.defaultBranch main
- git config --global user.name "ユーザー名"
- git config --global user.email "メールアドレス"　※GitHub登録で入手できる受信専用メールアドレスでよい（登録時に入力したメアドを公開不可にすると出てくる）

