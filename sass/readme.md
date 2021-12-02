### BEM
- `.Block--Element__Modifier`
- **scope**:

  - `l`: Layout, 
    - ex: `l-wrap` `l-container` `l-header`

  - `s | is | has`: State
    - ex: `is-active` `is-visible` `is-loading` `is-disabled`

  - `u`: Utility
    - ex: `u-clearfix`  `u-ellipsis`

  - `o`: Object
    - ex: `o-countdown`

  - `c`: Component
    - ex: `c-slider`  `c-dropMenu`

  - `js | j`

  - `t1 | s1`
    - 用來寫字體的，類似 `.h1`, `.h2`，但是 `.h1` 之類的跟標籤名耦合了，所以改用 `t1`
    - 通常拿來 mixin 會比較方便
      ```sass
      @mixin s1
          font-size: 14px
          line-height: 1.25

      h1, nav a
          +s1
      ```

  - `s`: scope
    - 某一塊的 css 都跟別人不一樣時，可以使用
    - 例如
      ```sass
      .s-content
        h1, h2, h3, h4, h5, h6
          +fz(30)
      ```

  - `_`: hack
    - 當需要臨時強制改某個東西時，少用，也不要拿這個來複用


  - `qa`: 給測試用的


### 書寫順序
- 定位屬性
  ```txt
    position
    display
    float
    left
    top
    right
    bottom
    overflow
    clear
    z-index
    clip
    visibility
  ```
- 自身屬性
  ```txt
    width
    height
    padding
    border
    margin
    background
  ```

- 文字樣式
  ```txt
    font-family
    font-size
    font-style
    font-weight
    font-varient
    color
  ```
  
- 文字屬性
  ```txt
    text-align 
    vertical-align 
    text-wrap 
    text-transform 
    text-indent 
    text-decoration 
    letter-spacing 
    word-spacing 
    white-space 
    text-overflow
  ```

- C3
  ```txt
    content 
    box-shadow
    border-radius
    transform
  ```

### 縮寫
```txt
  p / m: margin / padding
  t / r / l / b: top / right / left / bottom
  v / h || x / y: vertical / horizontal
  bg：background
```


### 常用英文
```txt
1. 頁面結構
  容器: container
  頁頭：header
  內容：content
  頁面主體：main
  頁尾：footer
  導航：nav
  側欄：sidebar
  欄目：column
  頁面外圍控制整體佈局寬度：wrapper
  左右中：left right center

2. 導航
  導航：nav
  主導航：mainbav
  子導航：subnav
  頂導航：topnav
  邊導航：sidebar
  左導航：leftsidebar
  右導航：rightsidebar
  菜單：menu
  子菜單：submenu
  標題: title
  摘要: summary

3. 功能
  標誌：logo
  廣告：banner
  登陸：login
  登錄條：loginbar
  註冊：regsiter
  搜索：search
  功能區：shop
  標題：title
  加入：joinus
  狀態：status
  按鈕：btn
  滾動：scroll
  標籤頁：tab
  文章列表：list
  提示信息：msg
  當前的: current
  小技巧：tips
  圖標: icon
  註釋：note
  指南：guild
  服務：service
  熱點：hot
  新聞：news
  下載：download
  投票：vote
  合作夥伴：partner
  友情鏈接：link || friendlink
  版權：copyright
  標示：sign || indication

4. 顏色
  4.1 功能:
    Brand
    Success
    Warning
    Danger
    Info

  4.2 主次色:
    Primary
    Regular
    Secondary
    Placeholder

  4.3 亮度:
    Base
    Light
    Lighter
    Extra Light
    Dark

5. 圖
  img-fluid      // 自適應圖 ( max-width: 100%, height: auto )
  img-thumbnail  // 縮略圖
```
