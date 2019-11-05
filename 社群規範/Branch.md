# 分支規範
因此建立時可以先在`local`建立分支，分支建立是依照[Using git-flow to automate your git branching workflow](https://jeffkreeftmeijer.com/git-flow/)、[Git Flow 是什麼?為什麼需要這種東西?](https://gitbook.tw/chapters/gitflow/why-need-git-flow.html)、[語意化版本](https://semver.org/lang/zh-TW/)、[版本規範](./Semantic Versioning.md)與[分支規範](./Branch.md)建立。

# 分支
主要有兩條，分別是`master`與`develop`，`develop`是從`master`分出來的，然後主要在所有變更與開發都在`develop`，這樣的好處是讓開發與穩定是分開，適合在社群開發上面。

 `featur/v使用的版本號(使用版本號還在想要不要，因為沒有試過)-發佈內容+使用者名稱`，可以參考。

那主要的運作方式是要修改是從 `develop` 開新分支 feature/xxxxxx 做修改，此時remote也是 feature/xxxxxx ，當完成後通過 git rebase 的方式與 develop 最新保持一致的版本，然後「拉請求」(pull requests)將 feature/xxxxxx 併入到 develop 。