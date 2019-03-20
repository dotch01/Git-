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

# Another common quetion

# Tags

# GitHub

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
