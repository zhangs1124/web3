# Git 操作指南

這個檔案包含了將您的程式碼變更提交 (Commit) 並上傳 (Push) 到 GitHub 的步驟。

請在 Visual Studio 的 "套件管理器主控台" (Package Manager Console) 或 "終端機" (Terminal) 中執行以下指令。

## 步驟 1: 檢查目前的狀態

在提交之前，先查看有哪些檔案被修改了。

```powershell
git status
```

您應該會看到紅色的檔案列表，這些是您修改過但還沒準備提交的檔案。

## 步驟 2: 將變更加入暫存區 (Stage)

將所有修改過的檔案加入到暫存區，準備進行提交。

```powershell
git add .
```

*注意：最後面的點 `.` 代表「當前目錄下的所有檔案」。*

再次執行 `git status`，您應該會看到檔案變成了綠色，表示已經準備好可以提交了。

## 步驟 3: 提交變更 (Commit)

將暫存區的檔案儲存為一個版本 (Commit)。請在引號中寫下清楚的註解。

```powershell
git commit -m "美化首頁與導航列配色，修復下拉選單問題"
```

## 步驟 4: 推送到 GitHub (Push)

將您的本地提交上傳到 GitHub 伺服器。

```powershell
git push
```

*或者如果這是您第一次在這個分支 push，可能需要使用：*
```powershell
git push -u origin main
```

---

## 常見問題

**Q: 如果 `git push` 失敗並顯示權限錯誤？**
A: 確保您的遠端儲存庫 URL 包含正確的 Token，或者您已經在電腦上登入過 GitHub。

**Q: 如果顯示 "nothing to commit"？**
A: 這表示您沒有任何新的變更需要儲存，或者您忘記執行 `git add .` 了。
