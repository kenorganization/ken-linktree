# 部署指南

## GitHub Pages 部署

### 前置準備

1. 擁有 GitHub 帳號
2. 安裝 Git
3. 準備好您的專案文件

### 步驟一：建立 GitHub 儲存庫

1. **登入 GitHub** 並點擊 "New repository"
2. **設定儲存庫名稱**：
   - 一般專案：`your-username.github.io`（主要頁面）
   - 專案頁面：`ken-linktree` 或其他名稱
3. **設定為 Public**（GitHub Pages 免費版要求）
4. **不要** 勾選 "Add a README file"
5. 點擊 "Create repository"

### 步驟二：上傳程式碼

```bash
# 初始化 Git 儲存庫
git init

# 添加所有文件
git add .

# 建立初始提交
git commit -m "Initial commit - Ken's Linktree v1.0.0"

# 設定主分支
git branch -M main

# 連接遠端儲存庫
git remote add origin https://github.com/yourusername/your-repo-name.git

# 推送到 GitHub
git push -u origin main
```

### 步驟三：啟用 GitHub Pages

1. **前往儲存庫設定**

   - 點擊儲存庫頁面上方的 "Settings" 標籤

2. **找到 Pages 設定**

   - 在左側選單中找到 "Pages"

3. **設定部署來源**

   - Source: "Deploy from a branch"
   - Branch: "main"
   - Folder: "/ (root)"

4. **儲存設定**

   - 點擊 "Save" 按鈕

5. **等待部署**
   - GitHub 會自動部署，通常需要 1-5 分鐘
   - 完成後會顯示網站 URL

### 步驟四：自定義網域（可選）

1. **購買網域**（如：your-name.com）

2. **設定 DNS 記錄**

   ```
   Type: CNAME
   Name: www
   Value: yourusername.github.io

   Type: A
   Name: @
   Values:
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```

3. **在 GitHub Pages 設定中添加自定義網域**
   - 在 "Custom domain" 欄位輸入您的網域
   - 勾選 "Enforce HTTPS"

## 其他部署選項

### Vercel 部署

1. **前往 [Vercel](https://vercel.com/)**
2. **使用 GitHub 帳號登入**
3. **點擊 "New Project"**
4. **選擇您的 GitHub 儲存庫**
5. **點擊 "Deploy"**

### Netlify 部署

1. **前往 [Netlify](https://netlify.com/)**
2. **點擊 "Add new site" > "Import an existing project"**
3. **選擇 GitHub 並授權**
4. **選擇您的儲存庫**
5. **設定建置選項**：
   - Build command: 留空
   - Publish directory: `.`
6. **點擊 "Deploy site"**

## 部署後檢查清單

- [ ] 網站可以正常訪問
- [ ] 所有連結都能正常工作
- [ ] 日夜模式切換功能正常
- [ ] 語言切換功能正常
- [ ] 分享功能在不同裝置上測試
- [ ] 響應式設計在各種螢幕尺寸下正常
- [ ] 頭像和圖片正常載入
- [ ] 社群媒體連結正確

## 常見問題

### Q: 為什麼我的網站顯示 404 錯誤？

A: 檢查以下項目：

- 確認 GitHub Pages 已啟用
- 確認主文件名為 `index.html`
- 等待 5-10 分鐘讓部署完成

### Q: 為什麼樣式沒有載入？

A: 檢查：

- CDN 連結是否正確
- 網路連線是否正常
- 瀏覽器是否阻擋了外部資源

### Q: 如何更新網站內容？

A:

```bash
# 修改文件後
git add .
git commit -m "Update content"
git push origin main
```

### Q: 可以使用免費的 SSL 憑證嗎？

A: GitHub Pages 自動提供免費的 SSL 憑證，只需在設定中勾選 "Enforce HTTPS"。

## 效能最佳化建議

1. **圖片最佳化**

   - 使用 WebP 格式
   - 壓縮圖片大小
   - 使用適當的尺寸

2. **載入速度最佳化**

   - 使用 CDN
   - 最小化 HTTP 請求
   - 啟用瀏覽器快取

3. **SEO 最佳化**
   - 添加適當的 meta 標籤
   - 使用語義化 HTML
   - 設定正確的 robots.txt

## 監控和分析

### Google Analytics 整合

```html
<!-- 在 </head> 標籤前添加 -->
<script
  async
  src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"
></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag() {
    dataLayer.push(arguments);
  }
  gtag("js", new Date());
  gtag("config", "GA_MEASUREMENT_ID");
</script>
```

### GitHub Insights

- 在儲存庫中查看流量統計
- 監控星標和分叉數量
- 檢查問題和貢獻

---

**更新日期：2025-07-12T00:00:00+08:00**
