# a.介紹你的設計理念，如何契合目標網站的內容或是風格?

### **遊戲化體驗**

**契合遊戲論壇主題**

遊戲論壇的用戶多為遊戲愛好者，對遊戲文化有高度認同感。因此，設計中加入 **復古像素風**、**經典遊戲梗** 或 **互動小遊戲**，能讓用戶感到親切並打發時間。

# **社群連結**

提供 **替代入口**（如 Discord 連結）或 **即時熱門話題預覽**，讓用戶在等待時仍能參與社群活動。

P.S.但是我沒正確導向，因為我沒有社群

# b.介紹該網頁使用到那些 HTML , CSS, ~~JavaScript~~，請用圖文並茂的方式分享。

### **HTML 部分**

1. **基本結構**：
    - `<!DOCTYPE html>`：聲明文檔類型為 HTML5。
    - `<html lang="zh-Hant">`：定義文檔的語言為繁體中文。
    - `<head>`：包含網頁的元數據，如字符集、視口設置、標題和樣式表。
    - `<body>`：包含網頁的主要內容。
2. **元數據**：
    - `<meta charset="UTF-8">`：設置字符編碼為 UTF-8。
    - `<meta name="viewport" content="width=device-width, initial-scale=1.0">`：確保網頁在移動設備上正確縮放。
    - `<title>`：設置網頁標題為「伺服器維修中」。
3. **內容結構**：
    - `<div class="retro-theme">`：用於包裹主要內容，並應用復古風格的主題樣式。
    - `<h1>` 和 `<p>`：用於顯示標題和段落文本。
    - `<button>`：創建一個按鈕，用於觸發攻擊 BOSS 的動作。
    
![螢幕擷取畫面 2025-03-04 191708](https://github.com/user-attachments/assets/27889f5a-3902-4019-b3a0-8ac41c07620d)

    
    - `<div>`：用於創建進度條、BOSS 血條、角色和 BOSS 的容器。
4. **動態元素**：
    - `<div class="pixel-art-progress-bar">`：顯示像素風格的進度條。
    - `<div id="boss-health-bar">`：顯示 BOSS 的血條。
    - `<div class="character">` 和 `<div class="boss">`：分別用於顯示角色和 BOSS 的動畫。
5. **連結**：
    - `<a>`：用於創建一個指向 Discord 臨時基地的連結。

---

# **CSS 部分**

1. **全局樣式**：
    - `html, body`：設置網頁的高度為 100%，移除默認的 margin，並禁止滾動。
    - `body`：設置字體、背景圖片、文字顏色、對齊方式，並使用 Flexbox 實現內容的垂直和水平居中。

1. **復古主題樣式**：
    - `.retro-theme`：設置背景顏色、內邊距、圓角和陰影，營造復古風格。
2. **進度條和血條**：
    - `.pixel-art-progress-bar` 和 `#boss-health-bar`：使用線性漸變（`linear-gradient`）來顯示進度和血條。
3. **按鈕樣式**：
    - `#click-to-attack`：設置按鈕的內邊距、字體大小、背景顏色、圓角和過渡效果。
    - `#click-to-attack:hover`：設置滑鼠懸停時的背景顏色變化。
4. **角色和 BOSS 動畫**：
    - `.character` 和 `.boss`：使用 `position: absolute` 將角色和 BOSS 固定在頁面底部，並設置動畫。
    - `@keyframes animateCharacter` 和 `@keyframes animateBoss`：定義角色和 BOSS 的動畫幀。
5. **動態效果**：
    - `transform: translateX(-50%) scale(2)`：用於放大角色。
    - `transition: left 0.5s ease`：實現角色移動的平滑過渡。
    - `animation`：用於播放角色攻擊和 BOSS 站立的動畫。
    
 ![螢幕擷取畫面 2025-03-04 191814](https://github.com/user-attachments/assets/f40142a3-5d88-4daa-a6d7-3735fb5b90e0)

    

---

### **JavaScript 部分**

1. **互動功能**：
    - `attackButton.addEventListener('click', () => { ... })`：監聽按鈕點擊事件，觸發角色攻擊動畫和 BOSS 血條更新。
    - `updateBossHealthBar()`：更新 BOSS 血條的顯示。
2. **動畫控制**：
    - 使用 `setTimeout` 來控制角色攻擊動畫的播放時間和返回原位。

---

# c. 需要包含 commit 次數的截圖 15
![image](https://github.com/user-attachments/assets/1c2ab565-5e29-42c7-9986-b6521eb9f3b6)
