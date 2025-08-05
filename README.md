# Ken's Personal Linktree

一個現代## 🛠️ 技術架構

- **前端框架**: 純 HTML5 + CSS3 + JavaScript (ES6+)
- **UI 框架**: Tailwind CSS + DaisyUI
- **圖示庫**: Font Awesome 6.4.0
- **影片系統**: 自開發 VideoBackgroundManager 類別
- **隨機演算法**: Fisher-Yates 洗牌演算法
- **響應式設計**: Mobile-first 設計理念
- **相容性**: 支援所有現代瀏覽器
- **Vanilla JavaScript**: 原生 ES6+ 語法，無依賴框架

### 背景影片技術

- **HTML5 Video API**: 原生影片播放控制
- **Fisher-Yates Algorithm**: 科學的隨機化演算法
- **Event-driven Architecture**: 事件驅動的播放管理
- **Error Recovery System**: 完整的錯誤處理和恢復機制
- **Performance Optimization**: 記憶體和效能最佳化 tree 設計，支持多語言、主題切換和背景影片功能。

## ✨ 功能特色

- 📱 **響應式設計**：完美支援各種設備
- 🌐 **繁體中文/英文雙語言支援**：一鍵切換語言
- 🌙 **深色/淺色主題切換**：自動儲存偏好設定
- 🎥 **動態背景影片播放系統**：Fisher-Yates 隨機演算法
- 🎨 **精美的 UI 設計**：完全仿照 Linktree
- 📤 **完整的社群分享功能**：支援 8 大平台
- 💾 **本地儲存使用者偏好設定**：記住您的選擇
- ⚡ **快速載入和流暢動畫**：1.5 秒超時保護，500ms 快速顯示
- 🔧 **完整的錯誤處理機制**：穩定可靠的運行
- 🎯 **載入時間最佳化**：積極預載策略，減少等待時間

## 🎬 背景影片系統

### 🎯 核心特色

- **Fisher-Yates 隨機演算法**: 確保真正隨機的影片播放順序
- **自動播放循環**: 影片結束自動播放下一個
- **錯誤處理**: 影片載入失敗自動跳過
- **頁面可見性控制**: 頁面隱藏時暫停播放，顯示時恢復
- **載入時間最佳化**: 1.5 秒超時保護，500ms 快速頁面顯示
- **積極預載策略**: preload="auto" 提升載入速度
- **流暢轉場效果**: 1-1.5 秒淡入淡出，減少等待感

### � 支援的影片格式

- **解析度**: HD (1080p) 到 UHD (4K)
- **幀率**: 24fps, 25fps, 30fps, 60fps
- **格式**: MP4 (H.264)
- **總計**: 36 個精選背景影片

## �️ 技術架構

- **前端框架**: 純 HTML5 + CSS3 + JavaScript (ES6+)
- **UI 框架**: Tailwind CSS + DaisyUI
- **圖示庫**: Font Awesome 6.4.0
- **影片系統**: 自開發 VideoBackgroundManager 類別
- **隨機演算法**: Fisher-Yates 洗牌演算法
- **響應式設計**: Mobile-first 設計理念
- **相容性**: 支援所有現代瀏覽器
- **Font Awesome**：豐富的圖示庫
- **Vanilla JavaScript**：原生 ES6+ 語法，無依賴框架

### 背景影片技術

- **HTML5 Video API**：原生影片播放控制
- **Fisher-Yates Algorithm**：科學的隨機化演算法
- **Event-driven Architecture**：事件驅動的播放管理
- **Performance Optimization**：記憶體和 CPU 使用最佳化
- **Loading Strategy**：多層次載入策略，500ms 快速顯示
- **Preload Optimization**：積極預載下一個影片，無縫切換
- **Timeout Protection**：1.5 秒超時保護，避免長時間等待

### 設計原則

- **Single Responsibility Principle**：單一職責原則
- **Open-Closed Principle**：開放封閉原則
- **DRY (Don't Repeat Yourself)**：避免程式碼重複
- **SOLID Principles**：遵循 SOLID 設計原則

## 📁 專案結構

```
ken-linktree/
├── index.html              # 主頁面檔案
├── README.md               # 專案說明文件
├── docs/                   # 文件目錄
│   ├── customization.md    # 客製化指南
│   └── deployment.md       # 部署指南
├── reports/                # 開發報告
│   └── development-report-*.md
├── scripts/                # 腳本檔案
│   └── main.js            # 主要 JavaScript 檔案 (已整合到 index.html)
└── src/                    # 原始檔案
    └── background-media/   # 背景影片檔案 (35個高品質影片)
        ├── 10110917-uhd_2160_3840_30fps.mp4
        ├── 10494882-uhd_2160_4096_25fps.mp4
        ├── ...其他33個影片檔案
```

## 🚀 快速開始

### 環境需求

- 現代瀏覽器 (Chrome 88+, Firefox 85+, Safari 14+, Edge 88+)
- HTTP 伺服器 (本地開發可使用 Live Server)
- 支援 ES6+ JavaScript 語法

### 安裝步驟

1. **複製專案**

   ```bash
   git clone [repository-url]
   cd ken-linktree
   ```

2. **啟動本地伺服器**

   ```bash
   # 使用 Python 3
   python -m http.server 8000

   # 使用 Node.js (需安裝 http-server)
   npx http-server

   # 使用 VS Code Live Server 延伸模組
   ```

3. **開啟瀏覽器**
   ```
   http://localhost:8000
   ```

## 🎨 客製化

### 個人資訊修改

編輯 `index.html` 檔案中的個人資訊區域：

```html
<!-- 個人資訊區域 -->
<div class="text-center mb-8">
  <div class="avatar mb-4">
    <div
      class="w-24 rounded-full ring ring-primary ring-offset-base-100 ring-offset-2"
    >
      <img
        src="https://avatars.githubusercontent.com/u/your-username"
        alt="個人頭像"
      />
    </div>
  </div>
  <h1 class="text-2xl font-bold text-base-content mb-2">你的名字</h1>
  <p class="text-base-content/70">你的簡介</p>
</div>
```

### 連結設定

修改 `LinktreeApp` 類別中的 `links` 陣列：

```javascript
this.links = [
  {
    title: "連結標題",
    url: "https://example.com",
    icon: "fas fa-icon-name",
    description: "連結描述",
  },
  // 添加更多連結...
];
```

### 背景影片管理

背景影片檔案位於 `src/background-media/` 目錄：

- 支援 MP4 格式
- 建議解析度：1080p 以上
- 建議時長：30-60 秒
- 自動循環播放

## 🔧 進階配置

### 主題客製化

在 `index.html` 中修改 CSS 自定義屬性：

```css
:root {
  --primary-color: #your-color;
  --secondary-color: #your-color;
  --accent-color: #your-color;
}
```

### 語言新增

在 `LinktreeApp` 類別中的 `translations` 物件新增語言：

```javascript
this.translations = {
  // 現有語言...
  "your-language": {
    // 翻譯內容...
  },
};
```

## 📊 效能監控

### 載入效能

- **首次內容繪製 (FCP)**：< 1.5 秒
- **最大內容繪製 (LCP)**：< 2.5 秒
- **首次輸入延遲 (FID)**：< 100 毫秒
- **累積版面偏移 (CLS)**：< 0.1

### 影片效能

- **記憶體使用**：< 200MB
- **CPU 使用率**：< 5%
- **網路頻寬**：自動調整品質

## 🤝 貢獻指南

1. Fork 專案
2. 建立功能分支 (`git checkout -b feature/AmazingFeature`)
3. 提交變更 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 開啟 Pull Request

## 📄 授權條款

此專案採用 MIT 授權條款 - 詳見 [LICENSE](LICENSE) 檔案

## 📞 聯絡資訊

- **開發者**：Ken
- **電子郵件**：[your-email@example.com]
- **GitHub**：[your-github-username]

## 🙏 致謝

- [Tailwind CSS](https://tailwindcss.com/) - CSS 框架
- [DaisyUI](https://daisyui.com/) - UI 元件庫
- [Font Awesome](https://fontawesome.com/) - 圖示庫
- [Pexels](https://www.pexels.com/) - 背景影片素材

---

⭐ 如果這個專案對你有幫助，請給我們一個星星！
