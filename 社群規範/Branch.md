主要有兩條，分別是 master 與 develop ， develop 是從 master 分出來的，然後主要在所有變更與開發都在 develop ，這樣的好處是讓開發與穩定是分開的，適合在眾多開發上面。

local要建立 `featur/v使用的版本號(使用版本號還在想要不要，因為沒有試過)-發佈內容+使用者名稱`，可以參考[語意化版本](https://semver.org/lang/zh-TW/)。

那主要的運作方式是要修改是從 `develop` 開新分支 feature/xxxxxx 做修改，此時remote也是 feature/xxxxxx ，當完成後通過 git rebase 的方式與 develop 最新保持一致的版本，然後「拉請求」(pull requests)將 feature/xxxxxx 併入到 develop 。