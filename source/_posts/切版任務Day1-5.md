---
title: 切版任務Day1~5分享
date: 2024-05-24 14:12:29
tags:
  - "切版任務"
  - "軟體工程師體驗營"
---

### 🏅 切版任務 Day1 - HTML 標籤元素、CSS 判斷

依照下列 HTML 與 CSS 程式碼內容判斷，請分享以下 HTML 標籤
a. `p`、`span`、`div`、`a` 各為什麼顏色

b. `p`、`span`、`div`、`a`、`img` 是區塊元素（block）還是行內元素 （inline）？

````htmlembedded=
<!-- HTML 程式碼 -->

<p class="green yellow orange">
我是P段落，文字顏色是什麼呢?區塊元素還是行內元素呢?
</p>
答案：green 區塊元素

<span class="red yellow green">
我是span，文字顏色是什麼呢?區塊元素還是行內元素呢?
</span>
答案：green 行內元素

<div class="blue orange red">
我是div，文字顏色是什麼呢?區塊元素還是行內元素呢?
</div>
答案：red 區塊元素

<a class="yellow blue green">
我是a連結，文字顏色是什麼呢?區塊元素還是行內元素呢?
</a>
答案：green 行內元素

<img src="..." alt="img">
我是img，區塊元素還是行內元素呢?
答案： 行內元素

```css=
/* CSS 程式碼 */

.orange {
    color: orange;
}

.blue {
    color: blue;
}

.red {
    color: red;
}

.yellow {
    color: yellow;
}

.green {
    color: green;
}
````

<!--more-->

### 參考解答

[Codepen](https://codepen.io/papa2415/pen/oNOVNeP)

### 🏅 切版任務 Day2 - 圖片處理技巧

#### 練習一：處理圖片下方的空隙

圖片預設下方會有 2 ~ 3px 空隙，請同學參考[此文章](https://tzuhui.github.io/2020/01/08/HTML/html-img-blank/)了解原理，
並回答下方問題。

#### 題目

嘗試在 .img 內加入 CSS 語法將圖片下的空白部分移除

[示意](https://codepen.io/hexschool/pen/mdXZJar)：
![](https://i.imgur.com/VggWh0X.png)

> 圖片下方與 p 標籤會有一小部分空隙

HTML：

```htmlembedded=
<img class="img" src="https://ithelp.ithome.com.tw/storage/image/logo.svg" alt="">
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo nostrum officiis aspernatur.</p>
```

CSS：

```css=
.img {
  display:block;
}
```

#### 練習二：圖片 hover 放大效果

當你將滑鼠移動到一個圖片上時，它會立即放大，通常會運用此方法來提供使用者互動回饋。

#### 題目

嘗試滑鼠 hover 在 .img 時，加入 CSS 語法讓圖片會有放大的效果

<img src="https://i.imgur.com/t2fEFtP.gif" width="250">

:::spoiler 提示：

- transform scale
  :::

### 參考解答

[Codepen](https://codepen.io/papa2415/pen/mdgomGx)

### 🏅 切版任務 Day3 - box-sizing

#### content-box

此為 box-sizing 屬性的預設值，width(寬)、height(高) 只包括內容本身的寬高，不包括 border、padding。
舉例：
當有一個 box 設定 `width: 30px; height: 20px; border: 10px solid black;`，
則此 box 總寬高：寬度: 50px, 高度: 40px

#### border-box

width(寬)、height(高) 除了內容本身的寬高，還包括 border、padding
舉例：
當有一個 box 設定 `width: 30px; height: 20px; border: 10px solid black; box-sizing: border-box;`，
則此 box 總寬高：寬度: 30px, 高度: 20px

#### 題目

請觀看此 [CodePen](https://codepen.io/hexschool/pen/yLvWLZY) 計算 .box1 與 .box2 的寬高（請不要用開發人員工具觀看）

### 參考解答

[Codepen](https://codepen.io/papa2415/pen/oNOOMWo)

### 🏅 切版任務 Day4 - HTML、CSS 文字設定與 margin、padding 運用

#### 問題

##### 1. 重要觀念選擇題

根據下列同樣的 A、B 模式，以 HTML 與 CSS 觀念中， HTML 決定了網頁的『架構』、CSS 形成網頁『樣式』，請問 A、B 各自最接近 HTML、CSS 差異描述，各為哪個?

```
1-- A 圖為 HTML，B 圖為 CSS
2-- A 圖為 CSS，B 圖為 HTML
3-- 他只是一隻尖叫的章魚，騙不了我((不可以選這個!))
```

![A 圖](https://i.imgur.com/phQ1SQh.png)　　　　　　![B 圖](https://i.imgur.com/WP8lOTY.png)

---

##### 2. 文字、間距相關運用

用 Codepen 練習下列的文字版面，練習文字相關尺寸設定、間距與相關 padding、margin 等運用。（可複製下方提供的文字練習）

![](https://i.imgur.com/tAJAG6m.png)

> [圖片連結](https://i.imgur.com/tAJAG6m.png)

內文文字與文字資訊提供如下：

```
六角學院
```

> 文字大小：`32px` `bold`｜顏色：`#000000`｜行高：`1.5` 倍

```
軟體工程師體驗營 - 一個月帶你做出網頁作品
```

> 文字大小：`24px` `bold`｜顏色：`#000000`｜行高：`1.5` 倍

```
（第一段）
Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt nostrum neque ipsam velit quibusdam delectus praesentium aut necessitatibus! Exercitationem, aperiam!

（第二段）
Mickey Mouse would have to be the main figure. Yet some mention must be made of our great animated classics. I made sketches of all the characters I thought should appear. Then, I called upon my modeling skills to build a one-16th-inch scale paper cut-out model of what I wanted. This was before photo-copying machines with reducing capabilities, so I had to make all the drawings in scale. Many of the figures had to be drawn, a quarter-inch high. The entire set was about 18-inches long by 3.5-inches high. But this model was a good tool for planning the show sequence and experimenting with different scenes.
```

> 文字大小：`20px`｜顏色：`#000000`、`#cd5e3c`｜行高：`1.5` 倍｜首行縮排：`36px`｜
> 橘色字為 `bold`

```
（右下連結）
前往頁面
```

> 寬度：`120px`｜文字置中｜文字大小：`16px`｜文字顏色：`#ffffff`｜行高：`1.5` 倍｜背景顏色：`#000000`
> hover 時：背景顏色：`#cd5e3c`

### 參考解答

[Codepen](https://codepen.io/papa2415/pen/poBmzRZ)

### 🏅 切版任務 Day5 - Material Icons + Figma Icon 名稱觀看教學

#### Material Icons

[Material Icon 官網](https://fonts.google.com/icons?icon.set=Material+Icons&icon.style=Filled)

> [Material Icons Guide](https://developers.google.com/fonts/docs/material_icons)
> 使用 Material Icon
> 使用 Filled style

**載入 Material Icon**

在 HTML `<head>` 內加入下方 CDN

```htmlembedded=
<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
```

使用 Codepen 時，也可以直接在設定中 CSS 區塊「Add External Stylesheets/Pens」加入 CDN URL（如圖）

![](https://i.imgur.com/vVB4njM.png)

**選擇想要使用的 Icon**
點選 icon，出現右側欄

![](https://i.imgur.com/MEfhxnE.png)

將 **Icon font** 中第一個區塊程式碼貼至 HTML 區塊內

> [Material Icons 載入範例](https://codepen.io/hexschool/pen/PoypBKv)

#### 題目

練習使用 **Material Icons** 載入下方 icon

![](https://imgur.com/CVp0Kgp.png)

> Arrow Forward、Arrow Downward、Menu、Close

#### 補充：Figma 如何觀看 icon 名稱

![](https://imgur.com/BdENbkZ.png)

> 設計師提供設計稿時，大多會有相關的導覽頁（guideline）提供相關基礎設定與相關資訊。

### 參考解答

[Codepen](https://codepen.io/papa2415/pen/gOyJeZQ)
