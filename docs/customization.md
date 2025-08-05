# 自定義指南

## 個人化設定

### 基本資訊修改

#### 1. 更新個人資訊

在 `index.html` 第 111-125 行附近找到並修改：

```html
<!-- 個人資訊 -->
<div class="text-center mb-8">
  <h1 class="text-3xl font-bold text-white mb-2">您的姓名</h1>
  <p class="text-white/80 mb-4">
    <span data-en="Your English bio here" data-zh="您的中文簡介">
      您的個人簡介
    </span>
  </p>
  <!-- Instagram 圖示 -->
  <div class="flex justify-center">
    <a
      href="https://instagram.com/yourusername"
      target="_blank"
      class="btn btn-circle btn-ghost hover:bg-white/20 text-white"
    >
      <i class="fab fa-instagram text-xl"></i>
    </a>
  </div>
</div>
```

#### 2. 更換頭像

找到第 105 行和第 214 行附近的頭像設定：

```html
<!-- 主要頭像 -->
<img src="您的頭像URL" alt="您的姓名's Avatar" />

<!-- Modal 中的頭像 -->
<img src="您的頭像URL" alt="您的姓名's Avatar" />
```

**推薦的頭像規格：**

- 尺寸：150x150 像素
- 格式：WebP 或 JPG
- 品質：高品質但檔案大小適中

### 連結管理

#### 添加新連結

在第 130-150 行附近的連結區域添加：

```html
<!-- 新連結範例 -->
<a
  href="您的連結URL"
  target="_blank"
  class="link-button btn btn-block bg-white/90 hover:bg-white border-0 text-gray-800 h-14 text-lg font-medium"
>
  <i class="fas fa-your-icon mr-2"></i>
  <span data-en="English Text" data-zh="中文文字">顯示文字</span>
</a>
```

#### 常用圖示選擇

```html
<!-- 社群媒體 -->
<i class="fab fa-facebook mr-2"></i>
<!-- Facebook -->
<i class="fab fa-twitter mr-2"></i>
<!-- Twitter -->
<i class="fab fa-linkedin mr-2"></i>
<!-- LinkedIn -->
<i class="fab fa-youtube mr-2"></i>
<!-- YouTube -->
<i class="fab fa-tiktok mr-2"></i>
<!-- TikTok -->
<i class="fab fa-discord mr-2"></i>
<!-- Discord -->

<!-- 專業服務 -->
<i class="fas fa-envelope mr-2"></i>
<!-- Email -->
<i class="fas fa-briefcase mr-2"></i>
<!-- Portfolio -->
<i class="fas fa-blog mr-2"></i>
<!-- Blog -->
<i class="fas fa-file-pdf mr-2"></i>
<!-- Resume/CV -->
<i class="fas fa-store mr-2"></i>
<!-- Shop -->

<!-- 其他 -->
<i class="fas fa-globe mr-2"></i>
<!-- Website -->
<i class="fas fa-phone mr-2"></i>
<!-- Phone -->
<i class="fas fa-map-marker-alt mr-2"></i>
<!-- Location -->
<i class="fas fa-calendar mr-2"></i>
<!-- Calendar -->
```

## 樣式自定義

### 配色方案修改

#### 1. 背景漸變

在 `<style>` 標籤中修改：

```css
/* 淺色模式背景 */
.gradient-bg {
  background: linear-gradient(
    45deg,
    #your-color1 0%,
    #your-color2 50%,
    #your-color3 100%
  );
}

/* 深色模式背景 */
.gradient-bg-dark {
  background: linear-gradient(
    45deg,
    #your-dark-color1 0%,
    #your-dark-color2 100%
  );
}
```

**推薦配色：**

- 粉色系：`#ff9a9e, #fecfef, #fecfef`
- 藍色系：`#667eea, #764ba2`
- 綠色系：`#11998e, #38ef7d`
- 紫色系：`#8360c3, #2ebf91`

#### 2. 按鈕樣式

修改連結按鈕的外觀：

```css
.link-button {
  /* 自定義背景色 */
  background: rgba(255, 255, 255, 0.95) !important;

  /* 自定義邊框 */
  border: 2px solid transparent !important;

  /* 自定義圓角 */
  border-radius: 15px !important;
}

.link-button:hover {
  /* 懸停效果 */
  background: #your-hover-color !important;
  transform: translateY(-3px);
  box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
}
```

#### 3. 頭像動畫

自定義頭像邊框動畫：

```css
.avatar-border::before {
  background: linear-gradient(
    45deg,
    #your-color1,
    #your-color2,
    #your-color3,
    #your-color4
  );
  animation: rotate 4s linear infinite; /* 調整動畫速度 */
}
```

### 字體自定義

#### 1. 使用 Google Fonts

在 `<head>` 標籤中添加：

```html
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link
  href="https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@300;400;500;700&display=swap"
  rel="stylesheet"
/>
```

然後在 CSS 中應用：

```css
body {
  font-family: "Noto Sans TC", sans-serif;
}
```

## 功能擴展

### 1. 添加新的社群媒體分享

在 JavaScript 中添加新的分享函數：

```javascript
/**
 * 分享到 Telegram
 */
shareToTelegram() {
    try {
        const text = encodeURIComponent(`Check out my Linktree: ${this.shareUrl}`);
        const telegramUrl = `https://t.me/share/url?url=${this.shareUrl}&text=${text}`;
        window.open(telegramUrl, '_blank');
        this.logger('已開啟 Telegram 分享', 'info');
    } catch (error) {
        this.logger(`Telegram 分享失敗: ${error.message}`, 'error');
        this.showToast('無法開啟 Telegram 分享', 'error');
    }
}
```

### 2. 添加點擊統計

```javascript
/**
 * 追蹤連結點擊
 */
trackLinkClick(linkName) {
    try {
        // 儲存到 localStorage
        const clicks = JSON.parse(localStorage.getItem('link-clicks') || '{}');
        clicks[linkName] = (clicks[linkName] || 0) + 1;
        localStorage.setItem('link-clicks', JSON.stringify(clicks));

        // 發送到 Google Analytics (如果有設定)
        if (typeof gtag !== 'undefined') {
            gtag('event', 'click', {
                'event_category': 'link',
                'event_label': linkName
            });
        }

        this.logger(`連結點擊追蹤: ${linkName}`, 'info');
    } catch (error) {
        this.logger(`追蹤失敗: ${error.message}`, 'error');
    }
}
```

### 3. 添加訪客計數器

```javascript
/**
 * 訪客計數器
 */
updateVisitorCount() {
    try {
        const today = new Date().toDateString();
        const visits = JSON.parse(localStorage.getItem('visitor-data') || '{}');

        if (visits.lastVisit !== today) {
            visits.totalVisits = (visits.totalVisits || 0) + 1;
            visits.lastVisit = today;
            localStorage.setItem('visitor-data', JSON.stringify(visits));
        }

        // 顯示訪客數（可選）
        const counter = document.getElementById('visitor-counter');
        if (counter) {
            counter.textContent = `訪客數：${visits.totalVisits}`;
        }
    } catch (error) {
        this.logger(`訪客計數失敗: ${error.message}`, 'error');
    }
}
```

## 多語言擴展

### 添加新語言

1. **修改語言切換邏輯**：

```javascript
toggleLanguage() {
    const languages = ['zh', 'en', 'ja']; // 添加日文
    const currentIndex = languages.indexOf(this.currentLanguage);
    const nextIndex = (currentIndex + 1) % languages.length;
    this.currentLanguage = languages[nextIndex];
    this.updateLanguage();
    this.saveUserPreferences();
}
```

2. **在 HTML 中添加新語言屬性**：

```html
<span data-en="Contact Me" data-zh="聯絡我" data-ja="お問い合わせ">聯絡我</span>
```

## SEO 最佳化

### 1. Meta 標籤優化

在 `<head>` 中添加：

```html
<!-- SEO Meta 標籤 -->
<meta name="description" content="您的個人簡介和連結集合" />
<meta name="keywords" content="您的姓名, 個人網站, 連結樹, linktree" />
<meta name="author" content="您的姓名" />

<!-- Open Graph 標籤 -->
<meta property="og:title" content="您的姓名's Linktree" />
<meta property="og:description" content="您的個人簡介" />
<meta property="og:image" content="您的頭像URL" />
<meta property="og:url" content="您的網站URL" />
<meta property="og:type" content="website" />

<!-- Twitter Card 標籤 -->
<meta name="twitter:card" content="summary_large_image" />
<meta name="twitter:title" content="您的姓名's Linktree" />
<meta name="twitter:description" content="您的個人簡介" />
<meta name="twitter:image" content="您的頭像URL" />
```

### 2. 結構化資料

```html
<script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "Person",
    "name": "您的姓名",
    "description": "您的個人簡介",
    "image": "您的頭像URL",
    "url": "您的網站URL",
    "sameAs": [
      "https://instagram.com/yourusername",
      "https://twitter.com/yourusername"
    ]
  }
</script>
```

## 測試和調試

### 本地測試環境

1. **使用 Python 簡易伺服器**：

   ```bash
   python -m http.server 8000
   ```

2. **使用 Node.js live-server**：
   ```bash
   npx live-server
   ```

### 跨瀏覽器測試

- Chrome DevTools 設備模擬
- Firefox 響應式設計模式
- Safari Web Inspector
- 實際手機測試

### 效能測試工具

- Google PageSpeed Insights
- GTmetrix
- WebPageTest
- Lighthouse

---

**更新日期：2025-07-12T00:00:00+08:00**
