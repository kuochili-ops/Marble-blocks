# 𓃥 白六管道積木 (3D Marble Run Blocks)

![Three.js](https://img.shields.io/badge/Three.js-r128-black?style=flat-square&logo=three.js)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-v3-38bdf8?style=flat-square&logo=tailwindcss)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

一個基於 WebGL 與 Three.js 開發的 3D 管道積木拼裝與彈珠滾動模擬器。使用者可以在網頁中自由建構複雜的 3D 管道迷宮，並投放彈珠觀察其流暢的物理動能與自動傳送過程。

👉 **[立即線上體驗 Live Demo](https://kuochili-ops.github.io/Marble-blocks/)**

---

## 🌟 專案亮點與核心特色

* 🔮 **預設全透視管道外觀**：積木外殼預設採用透明半高亮質感，能清晰觀察彈珠在管道內部運轉與流暢出彎的軌跡。
* 🌀 **動能強化螺旋升降梯**：具備強迫接軌與動能爆發機制，彈珠進入升降梯頂端後會自動滑入接軌彎管，順暢完成循環。
* 🎯 **智慧自動吸附對齊**：新增積木時會自動偵測相鄰管道開口，自動轉向並貼合開口，建構連貫軌道超輕鬆。
* 🎥 **第一人稱彈珠追蹤攝影機**：開啟追蹤模式後，鏡頭會跟隨彈珠穿梭於 3D 迷宮之間，帶來極具沉浸感的視角體驗。
* 🔗 **極短網址與 JSON 導出/匯入**：採用 LZ-String 高效壓縮演算法，可將完整的 3D 軌道結構資料壓縮並轉換為超短連結分享給好友。
* 📱 **全平台觸控與響應式支援**：專為手機與桌面端優化，支援直覺的 3D 視角旋轉、縮放以及 Gizmo 軸向平移操作。

---

## 🧩 積木種類介紹

| 積木類型 | 特色說明 |
| :--- | :--- |
| **直管積木 (Straight)** | 對立面貫穿相通，提供基礎的直線加速與銜接。 |
| **彎管積木 (Curved)** | 鄰接面 90° 弧形轉彎，內建平滑動能補償，確保彈珠順暢出彎。 |
| **十字管積木 (Cross)** | 兩軸平面十字交叉管道，可實現多路徑交叉與分流。 |
| **螺旋升降梯 (Lift)** | 動力升降模組，可自動將抵達底部的彈珠推升至頂端進行高低差循環。 |

---

## 🎮 操作指南

### 1. 軌道建構與編輯
* **新增積木**：點擊右下角「新增積木」按鈕選擇種類，積木將自動新增至最佳對接位置。
* **移動積木**：點擊選取積木後，拖曳 3D 軸向箭頭（Gizmo）即可在網格空間中精確位移。
* **旋轉與替換**：使用底部工具列可針對 X / Y / Z 軸進行 90° 旋轉，或隨時更換積木型態。
* **隱藏外殼**：點擊頂部「眼睛」圖示可切換透明外殼顯示，享受純粹的管道幾何美感。

### 2. 彈珠投放與追蹤
* **放彈珠模式**：點擊頂部「放彈珠」按鈕，畫面上會標示出所有開放的管道入口（黃色亮環），點擊即可投放彈珠。
* **追蹤攝影機**：點擊頂部「攝影機」圖示進入追蹤模式，投放彈珠後鏡頭將自動跟隨彈珠移動。

---

## 🛠️ 技術架構

* **3D 渲染引擎**：[Three.js (r128)](https://threejs.org/)
* **控制器與物理體驗**：`OrbitControls`, 自研管道插值導向 (Bezier/Catmull-Rom Path) 與碰撞反應機制
* **UI 樣式與圖示**：[Tailwind CSS](https://tailwindcss.com/), [Lucide Icons](https://lucide.dev/)
* **資料壓縮與分享**：[LZ-String](https://github.com/pieroxy/lz-string)

---

## 🚀 本地開發與部署

本專案為純前端單頁應用程式（SPA），無需複雜的建置環境，直接開啟即可執行：

1. **複製專案庫**
   ```bash
   git clone [https://github.com/kuochili-ops/Marble-blocks.git](https://github.com/kuochili-ops/Marble-blocks.git)
   cd Marble-blocks
