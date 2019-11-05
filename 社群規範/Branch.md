# 分支規範
在敏捷攀術團隊中分支建立是依照[A successful Git branching model](https://nvie.com/posts/a-successful-git-branching-model/)、[語意化版本](https://semver.org/lang/zh-TW/)、[版本規範](./Semantic Versioning.md)與[分支規範](./Branch.md)建立。  

其原因是與用法可以參考[Git Flow 是什麼?為什麼需要這種東西?](https://gitbook.tw/chapters/gitflow/why-need-git-flow.html)、[Using git-flow to automate your git branching workflow](https://jeffkreeftmeijer.com/git-flow/)，實際完對運用方法會在下面詳細提出，如果有更好的方式可以在「議題」(Issues)提出。  

# 分支
主要有兩條，分別是`master`與`develop`，`develop`是從`master`分出來的，然後主要在所有變更與開發都在`develop`，這樣的好處是讓開發與穩定是分開，適合在社群開發上面。

 `featur/v使用的版本號(使用版本號還在想要不要，因為沒有試過)-發佈內容+使用者名稱`，可以參考。

那主要的運作方式是要修改是從 `develop` 開新分支 feature/xxxxxx 做修改，此時remote也是 feature/xxxxxx ，當完成後通過 git rebase 的方式與 develop 最新保持一致的版本，然後「拉請求」(pull requests)將 feature/xxxxxx 併入到 develop 。

我突然想要為什麼以前合併會有問題，因為我沒有做分支保護，所以合併時會出現問題，其中原因是沒有使用 git rebase 來讓 develop 成為我的基礎版本，那時候還不會那個指令，所以常常會出現問題，後期為了解決這個問題我使用 git merge 來同步develop，但那個就不是我從它那邊最新版去修改了。

