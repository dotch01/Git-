# Git commit command


<html>
  <body>
    <div style="font-size=20px;">
      <div>git init 初始化 git 要備份的目錄</div>
      <div>git status 查看資料夾狀態</div>
      <div>echo "hello, git" > costom.html 新增檔案</div>
      <div>git add costom.html 新增給 git 管理的檔案</div>
      <div>git add *.(副檔名) 一次新增某種副檔名的檔案給 git 管理</div>
      <div>git add --all 將資料夾內全部檔案新增給 git 管理</div>
      <div>git commit -m "更改了甚麼的訊息" 執行commit 指令</div>
      <div>git commit -a -m "更改了甚麼的訊息" 參數只對已經存在 Repository 的檔案有效，對新加入的檔案是無效的</div>
      <div>git log 查看專案的更改變動訊息</div>
      <div>git log --oneline --graph 查看更精簡的訊息</div>
      <div>git log --oneline --author="名字\|名字" 查看某位作者(或另一位)的 Commit</div>
      <div>git log --oneline --grep="訊息" 可以從 Commit 訊息裡面搜尋符合字樣的內容</div>
      <div>git log -S "訊息" 可以搜尋所有 Commit 的檔案</div>
      <div>git log --oneline --since="9am" --until="12am" --after="2017-01" 這樣可以找到「從 2017 年 1 月之後，每天早上 9 點到 12 點的 Commit」</div>
      <div>git rm 檔案名稱.副檔名 不需要再 add 就可以直接加入暫存區</div>
      <div>git rm 檔案名稱.副檔名 --cached 讓檔案不再被git控管，當 .gitgnore無法忽略某檔案時，可用此指令移出他</div>
      <div>git mv A.副檔名 B.副檔名 把A檔案改名成B檔案，不需要 add</div>
      <div>git commit --amend -m "更正的訊息" 修改最後一次 commit 的訊息</div>
      <div>git commit --amend --no-edit 把不想新增 commit 的檔案 add 後跟最後一次的 commit 合併</div>
      <div>touch 目錄名稱/隨便一個檔案 在原本 git 控管目錄下新增資料夾後新增檔案，git 就可以知道資料夾的存在</div>
      <div>touch .gitignore 讓 git 忽略的檔案都要在此檔內編輯，檔名.副檔名、目錄/檔名.副檔名</div>
      <div>git add -f 檔案名稱 忽略 .gitignore 的忽略規則</div>
      <div>git clean -fX 強制刪除被 .gitignore 忽略的檔案</div>
      <div>git log 檔名.副檔名 查看此檔案的 commit 紀錄，git log -p 可詳細察看每次 commit 做了甚麼更改</div>
      <div>git blame 檔名.副檔名 能知道某個檔案的某一行是誰寫的， blame 後面加上 -L 行數,行數 查看特定的某幾行</div>
      <div>git checkout 檔名.副檔名 救回某個被刪除的檔案， checout 後面+ . 可以把所有被 del 的檔案救回</div>
      <div>git checkout HEAD~2(代表幾個版本以前) 把以前版本的某個或某些檔案還原到目錄下</div>
      <div>git reset (用log查看的編號)+上箭頭或~數字 拆除 Commit，一個^代表回到前幾次，通常超過2次會寫成~3</div>
      <div>git reset (用log查看的編號) 回到指定的Commit</div>
      <div>git reset 模式補充 Commit拆出來的檔案 --mixed 檔案丟回工作目錄 --soft 丟回暫存區 --hard 直接丟掉</div>
      <div>git add -p 檔名.副檔名 只 commit 部分 code</div>
    </div>
  </body>
</html>

# Git branch command

<html>
  <body>
    <div style="font-size=20px;">
      <div>git reflog 查看被 --hard清除的 commit 在用git reset (用reflog查看的編號) --hard 可回到比較新的版本</div>
      <div>cat .git/refs/heads/master 查看 master 分支編碼</div>
      <div>git branch 查看目前所在分支和所有分支</div>
      <div>git checkout [分支名稱] 切換分支</div>
      <div>git branch [取分支名稱] 加入新分支</div>
      <div>git branch -m [分支名稱] [更改成此名] 更改分支名稱</div>
      <div>git branch -d [分支名稱] 刪除分支，大寫D可以強制刪除</div>
      <div>git merge [分支名稱] 合併分支，要先切回去要合併的分支</div>
      <div>git merge [分支名稱] --no-f 不要使用快轉模式，可以讓合回master的分支畫出小耳朵</div>
      <div>git branch [取分支名稱] [SHA-1編碼] </div>
      <div>git rebase [分支名稱] 合併分支，把目前所在分支合到指定的分支去，重新產生SHA-1編碼</div>
      <div>git reset ORIG_HEAD --hard 跳回 rebase 前的狀態</div>
      <div>git checkout --ours(--theirs) [檔名.副檔名] 決定要使用我或對方分支的二進位檔(例如圖片)</div>
      <div>@ 可以取代HEAD使用</div>
      <div>git branch [取分支名稱] [SHA-1編碼] 回到過去某個 commit 開啟分支</div>
      <div>git checkout -b [取分支名稱] [SHA-1編碼] 回到過去某個 commit 開啟分支，並直接跳轉過去</div>
    </div>
  </body>
</html>

# Modify history message 

<html>
  <body>
    <div style="font-size=20px;">
      <div>git rebase -i [SHA-1編碼]  進入 Rebase 的互動模式 Rebase 指令的應用範圍會，從現在到指定編碼時，要更改的 commit 前面改成 r 就會進入 vim 編輯器</div>
      <div>squash 進入 Rebase 的互動模式後，在編碼前輸入 squash 就會往上合併 commit </div>
      <div>進入 Rebase 的互動模式後，在編碼前輸入 edit 在使用 git reset HEAD^ 跑完之後重新 add+commit 後記得 git rebase --continue 讓 rebase 跑完就可以把 commit 拆成多個了</div>
      <div>進入 Rebase 的互動模式後，在編碼前輸入 edit ，然後繼續 git rebase --continue 後新增檔案+add+commit 在git rebase --continue 後就成功在歷史紀錄裡新增 commit 了</div>
      <div>git rebase -i [SHA-1編碼] 進入 Rebase 的互動模式後，移動 commit 紀錄的順序(從上到下是舊到新)存檔退出後再執行一次 git rebase -i [SHA-1編碼] 就可更改 commit 順序</div>
      <div>若要刪除 commit 及是刪除 commit 紀錄後存檔離開再次執行指令即可</div>
      <div>git revert HEAD --no-edit 取消最後一次的 commit 並不要編輯訊息，但會增加一個 commit 且不會刪除不要的 commit</div>
    </div>
  </body>
</html>

# Another common quetion

<html>
  <body>
    <div style="font-size=20px;">
      <div>git stash 先把做到一半的東西存起來，沒有add的文件要加上 -u </div>
      <div>git stash list 查看存放到 stash 的檔案</div>
      <div>git stash pop stash@{[存放順序數字]} 跳回去某個工作進度然後刪除這個存放的進度</div>
      <div>git stash drop stash@{[存放順序數字]} 刪掉存放的進度</div>
      <div>git stash apply stash@{[存放順序數字]} 跳回去某個工作進度</div>
      <div>git filter-branch --tree-filter "終端指令" 可以用後面的指令去每個 commit 跑過一遍</div>
      <div>git reset refs/original/refs/heads/master --hard 重新回去執行 filter-branch 前的狀態</div>
      <div>git cherry-pick [SHA-1編碼] ... 可以簡某個分支的 commit 過來直接合併，加上 --no-commit 會先放到暫存區 不會直接合併</div>
      <div>git filter-branch -f --tree-filter "終端指令" 可以用後面的指令去每個 commit 跑過一遍，並刪除備份點，再來 del .git/refs/original/refs/heads/master，刪除 git 備份點，在 git reflog expire --all --expire=now 強制 reflog 過期，最後 git gc --prune=now 清理垃圾，就可以清理乾淨要rm的檔案囉</div>
      <div>git fsck 查看垃圾空間</div>
    </div>
  </body>
</html>

# Tags

<html>
  <body>
    <div style="font-size=20px;">
      <div>git tag [標籤名稱] [SHA-1編碼] 幫某個 commit 貼上標籤</div>
      <div>git tag [標籤名稱] [SHA-1編碼] -a -m "訊息" 幫某個 commit 貼上標籤並附上訊息</div>
      <div>git tag -d [標籤名稱] 刪除標籤</div>
      <div>分支會隨著 commit 移動但標籤不會</div>
    </div>
  </body>
</html>

# GitHub

<html>
  <body>
    <div style="font-size=20px;">
      <div></div>
      <div></div>
      <div></div>
      <div></div>
      <div></div>
      <div></div>
      <div></div>
      <div></div>
      <div></div>
      <div></div>
      <div></div>
      <div></div>
      <div></div>
      <div></div>
      <div></div>
      <div></div>
      <div></div>
      <div></div>
    </div>
  </body>
</html>

# Terminal command

<html>
  <body>
    <div style="font-size=20px;">
      <div>cd /路徑名稱/... 移動到目錄</div>
      <div>cd 查看當前存在目錄</div>
      <div>cd .. 往上一層目錄移動</div>
      <div>mkdir 建立資料夾</div>
      <div>dir 列出目前檔案列表</div>
      <div>dir -al 列出目前檔案列表，a 是指連小數點開頭的檔案（例如.gitignore）也會顯示，l 則是完整檔案的權限、擁有者以及建立、修改時間</div>
      <div>copy 複製檔案</div>
      <div>move 移動檔案</div>
      <div>mv A.html B.html 把A更名成B</div>
      <div>del 刪除檔案</div>
      <div>cls 清除畫面上內容(好看用，跟檔案無關)</div>
    </div>
  </body>
</html>
