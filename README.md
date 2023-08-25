# tastyLog

# Subversion から　 Git

# ブランチ戦略
```
> Git-flow
main
hotfix : 緊急対応を行い、mainとbranchを削除(branchは削除)
release : リリース準備(v1.0のタグ付け)し、整えばdevとmainへ(branchは削除)
develop : 開発中のマスタ(常に動作する)
feature : 機能ごとにブランチを切る(branchは削除)


> GitHub-flow
main : 常にデプロイ可能
feature : 機能ごとにブランチを切る(branchは削除)


> GitLab-flow
- productionブランチモデル(開発とリリースのタイミングでズレがあるケースで利用)
main : 現行??
feature : 機能修正
production : v1.0のような原稿リリース


- 環境ブランチモデル(環境ごとにリリースを管理したいケースで利用)
main > staging > productionの順
main : 
feature : 
staging : stagingで様子見
production : リリース


- releaseブランチモデル(外部リリース単位で管理したいケースで利用)
*nodeのバージョン対応や会社別の対応など
main : 
feature(複数) : 
stable(複数) : 


```

# ブランチ保護

```
.github/CODEOWNERS
 全ソースのオーナーがuser1とuser2  *はマッチ条件　そのたとにオーナー　記述は後勝ち
 *    @user1 @user2

 拡張子が .jsのファイル
 *.js    @js-owner

 /docs/ディレクトリ以下のすべてのファイル
 /docs/  @doctocat


```