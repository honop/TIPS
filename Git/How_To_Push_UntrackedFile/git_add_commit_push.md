# git add、commit、pushのやり方

## やりたいこと
* ローカルリポジトリ内の新たなファイルをリモートリポジトリにアップすること


## 前提として
* git cloneを用いて既にリモートリポジトリとローカルリポジトリを同期させていることが必要。やり方はGit_Clone.mdにて。

## やり方
1. まずcdコマンドでローカルリポジトリに移動する。
    <img alt="qiita-square" src="pics/cd.png">
    ↑移動できた。

2. git statusでUntrackedFileの確認
    <img alt="qiita-square" src="pics/UntrackedFile.png">
    まだローカルのgitに反映されていないファイルの一覧が表示された。

3. git add -iで対話モードに移行する
    <img alt="qiita-square" src="pics/gitadd1.png">
    ここで、4と打つとuntracked fileが羅列される
    <img alt="qiita-square" src="pics/gitadd2.png">
    ```
    Add untracked>> 
    ```
    と表示されるので、Allの意味を持つ*(アスタリスク)を打つと、無事ローカルリポジトリに全てのフォルダが保存される。  
    対話モードを終了させるためにはqを打つ。

4. git add .をする  
    ```
    git add .  
    git commit -m "お好きなコメント何でも"
    ```
    と打つ
    <img alt="qiita-square" src="pics/gitadd3.png">

5. git pushをする
    <img alt="qiita-square" src="pics/push.png">
    mainに反映させるため、
    ```  
    git push origin main  
    ```
    と打つ
    <img alt="qiita-square" src="pics/gitpush.png">
    <img alt="qiita-square" src="pics/pushdone.png">
    ↑無事リモートリポジトリにも新規ファイルが反映された！


