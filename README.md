# 前端檢查清單

[![Join the chat at https://gitter.im/Front-End-Checklist/Lobby](https://badges.gitter.im/Front-End-Checklist/Lobby.svg)](https://gitter.im/Front-End-Checklist/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![Front‑End_Checklist followed](https://img.shields.io/badge/Front‑End_Checklist-followed-brightgreen.svg)](https://github.com/thedaviddias/Front-End-Checklist/)
[![Contributors](https://img.shields.io/github/contributors/thedaviddias/Front-End-Checklist.svg)](https://github.com/thedaviddias/Front-End-Checklist/graphs/contributors)
[![CC0](https://img.shields.io/badge/license-CC0-green.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

The **Front-End Checklist** is an exhaustive list of all elements you need to have / to test before launching your site / page HTML to production.
這個 **前端檢查清單** 是個所有要素你須要有檢驗的全面清單，在啟動你的網站 / 頁面 HTML 到產品之前.

It is based on Front-End developers' years of experience, with the additions coming from some other open-source checklists.
他是基於前端開發的多年經驗,隨著從一些其他開源檢查清單增加.

## 內容目錄

1. **[Head](#head)**
2. **[HTML](#html)**
3. **[網頁字體](#webfonts)**
4. **[CSS](#css)**
5. **[圖像](#images)**
6. **[JavaScript](#javascript)**
7. **[安全性](#security)**
8. **[效能](#performance-1)**
9. **[易用性](#accessibility)**
10. **[SEO](#seo)**

## 如何使用?

All items in the **Front-End Checklist** are required for the majority of the projects, but some elements can be omitted or are not essential (in the case of an administration web app, you may not need RSS feed for example). We choose to use 3 levels of flexibility:
所有項目在這個 **前端檢查表** 中被要求對於大多數的專案, 但有些元素可以被忽略或不是完全必要的(舉例來說在這一個管理網頁應用程式的例子裡, 你也許不需要 RSS 訂閱). 我們選擇使用彈性的三個等級:

* ![Low][low_img] means that the item is **recommended** but can be omitted in some particular situations.
* ![Low][low_img] 意味著這個項目是 **被推薦的** 但可以被忽略在有些特定的情況.
* ![Medium][medium_img] means that the item is **highly recommended** and can eventually be omitted in some really particular cases. Some elements, if omitted, can have bad repercussions in terms of performance or SEO.
* ![Medium][medium_img] 意味著這個項目是 **高度被推薦的** 以及可以最終被忽略在有些真正地特定的例子中. 有些要素, 如果忽略, 可能有壞的影響在項目的效能或 SEO 中.
* ![High][high_img] means that the item **can't be omitted** by any reason. You may cause a dysfunction in your page or have accessibility or SEO issues. The testing priority needs to be on these elements first.
* ![High][high_img] 意味著這個項目是 **不能被忽略** 依據任何理由. 你也許引起一個功能障礙在你的頁面或有無障礙或 SEO 議題.這個檢驗優先級必須是首要的在那些要素之上.


Some resources possess an emoticon to help you understand which type of content / help you may find on the checklist:
有些資源擁有一個表情符號為了幫助你了解內容的種類 / 為了幫助你可以在這個檢查表上發現:

* 📖: documentation or article
* 📖: 文件 or 文章
* 🛠: online tool / testing tool
* 🛠: 線上工具 / 檢驗工具
* 📹: media or video content
* 📹: 媒體或影片內容

---

## Head

> **注意:** 你可以發現 [每件事的一個清單](https://github.com/joshbuchea/HEAD) 可以被發現在這個 `<head>` 中的一個 HTML 文件.

### Meta 標籤

* [ ] **Doctype:** ![High][high_img] The Doctype is HTML5 and is at the top of all your HTML pages.
* [ ] **文件種類:** ![High][high_img] 這個文件種類是 HTML5 以及是在這個頂部的所有你的 HTML 頁面.

```html
<!-- Doctype HTML5 -->
<!-- 文件種類 HTML5 -->
<!doctype html>
```


> 📖 [確定最少字符編碼 - HTML5 W3C](https://www.w3.org/TR/html5/syntax.html#determining-the-character-encoding)


*The next 3 meta tags (Charset, X-UA Compatible and Viewport) need to come first in the head.*
*接下來的 3 個 meta 標籤 (Charset, X-UA Compatible and Viewport) need to come first in the head.*

* [ ] **Charset:** ![High][high_img] The charset declared (UTF-8) is declared correctly.
* [ ] **Charset:** ![High][high_img] 這個 charset 宣告 (UTF-8) 被宣告正確地.

```html
<!-- Set character encoding for the document -->
<!-- 設定字符編碼給這個文件 -->
<meta charset="utf-8">
```

* [ ] **X-UA-Compatible:** ![Medium][medium_img] The X-UA-Compatible meta tag is present.
* [ ] **X-UA-Compatible:** ![Medium][medium_img] 這個 X-UA-Compatible meta 標籤出現在.

```html
<!-- Instruct Internet Explorer to use its latest rendering engine -->
<!-- 通知 IE 使用它的最新版渲染引擎 -->
<meta http-equiv="x-ua-compatible" content="ie=edge">
```

> 📖 [指定傳統文件模式 (Internet Explorer)](https://msdn.microsoft.com/en-us/library/jj676915(v=vs.85).aspx)


* [ ] **Viewport:** ![High][high_img] The viewport is declared correctly.
* [ ] **視埠:** ![High][high_img] 這個視埠被正確地宣告.

```html
<!-- Viewport for responsive web design -->
<!-- 視埠為了響應式網頁設計 -->
<meta name="viewport" content="width=device-width, initial-scale=1">
```

* [ ] **Title:** ![High][high_img] A title is used on all pages (SEO: Google calculate the pixel width of the characters used in the title, cut off between 472 and 482 pixels. Average character limit would be around 55-characters).
* [ ] **標題:** ![High][high_img] 一個標題被用來在每個頁面上 (SEO: Google 計算像素寬度的字符使用在標題中, 減少在 472 以及 482 像素之間. 平均字符限制將會是約 55 個字符).

```html
<!-- Document Title -->
<!-- 文件標題 -->
<title>Page Title less than 65 characters 頁面標題少於 65 字符</title>
```

> 📖 [Title - HTML - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/title)


* [ ] **Description:** ![High][high_img] A meta description is provided, it is unique and doesn't possess more than 150 characters.
* [ ] **描述:** ![High][high_img] 一個 meta 描述被提供, 他是獨一和不擁有超過 150 字符.

```html
<!-- Meta Description -->
<!-- Meta 描述 -->
<meta name="description" content="Description of the page less than 150 characters 頁面少於 150 字符的描述">
```

* [ ] **Favicons:** ![Medium][medium_img] Each favicon has been created and displays correctly. If you have only a `favicon.ico`, put it at the root of your site. Normally you won't need to use any markup. However, it's still good practice to link to it using the example below. Today, **PNG format is recommended** over `.ico` format (dimensions: 32x32px).
* [ ] **網站圖示:** ![Medium][medium_img] 每個網站圖示 已經被創造和顯示正確. 如果你只有一個 `favicon.ico`, 放置它在你的網站根目錄. 正常情況下你不必使用任何標記. 然而, 使用下面的示例鏈接到它仍然是好的練習. 今天, **PNG 格式被推薦** 超過 `.ico` 格式 (尺寸: 32x32px).

```html
<!-- Standard favicon -->
<!-- 標準網站圖示 -->
<link rel="icon" type="image/x-icon" href="https://example.com/favicon.ico">
<!-- Recommended favicon format -->
<!-- 推薦網站圖示格式 -->
<link rel="icon" type="image/png" href="https://example.com/favicon.png">
```

> * 🛠 [Favicon Generator](https://www.favicon-generator.org/)
> * 🛠 [網站圖示產生器](https://www.favicon-generator.org/)
> * 🛠 [RealFaviconGenerator](https://realfavicongenerator.net/)
> * 🛠 [真的網站圖示產生器](https://realfavicongenerator.net/)
> * 📖 [Favicon Cheat Sheet](https://github.com/audreyr/favicon-cheat-sheet)
> * 📖 [網站圖示備忘表](https://github.com/audreyr/favicon-cheat-sheet)
> * 📖 [Favicons, Touch Icons, Tile Icons, etc. Which Do You Need? - CSS Tricks](https://css-tricks.com/favicon-quiz/)
> * 📖 [網站圖示, 觸碰圖像, 瓦片圖像, 等等. 你需要哪個? - CSS Tricks](https://css-tricks.com/favicon-quiz/)
> * 📖 [PNG favicons - caniuse](https://caniuse.com/#feat=link-icon-png)
> * 📖 [PNG favicons - caniuse](https://caniuse.com/#feat=link-icon-png)

* [ ] **Apple Touch Icon:** ![Low][low_img] Apple touch favicon apple-mobile-web-app-capable are present. *(Create your Apple Icon file with at least 200x200px dimension to support all dimensions that you may need)*
* [ ] **蘋果觸碰圖像:** ![Low][low_img] 蘋果觸碰網站圖像出現在 蘋果-移動-網頁-應用程式-能力. *(創建你的蘋果圖像檔案用至少 200x200px 尺寸來支持所有尺寸你可能需要)*

```html
<!-- Apple Touch Icon -->
<!-- 蘋果觸碰圖像 -->
<link rel="apple-touch-icon" href="/custom-icon.png">
```

> 📖 [配置網頁應用程式](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html)


- [ ] **Windows Tiles:**![Low][low_img] Windows tiles are present and linked.
- [ ] **視窗瓦片:**![Low][low_img] 視窗瓦片鏈結和出現在.

```html
<!-- Microsoft Tiles -->
<!-- 微軟瓦片 -->
<meta name="msapplication-config" content="browserconfig.xml" />
```

Minimum required xml markup for the browserconfig.xml file is as follows:
browserconfig.xml 檔案的最小所需 xml 標記如下:


```xml
<?xml version="1.0" encoding="utf-8"?>
<browserconfig>
   <msapplication>
     <tile>
        <square70x70logo src="small.png"/>
        <square150x150logo src="medium.png"/>
        <wide310x150logo src="wide.png"/>
        <square310x310logo src="large.png"/>
     </tile>
   </msapplication>
</browserconfig>
```

> 📖 [瀏覽器配置 schema 參考](https://msdn.microsoft.com/en-us/library/dn320426(v=vs.85).aspx)


* [ ] **Canonical:** ![Medium][medium_img] Use `rel="canonical"` to avoid duplicate content.
* [ ] **典範:** ![Medium][medium_img] 使用 `rel="canonical"` 避免複製內容.

```html
<!-- Helps prevent duplicate content issues -->
<!-- 幫助避免重複內容議題 -->
<link rel="canonical" href="http://example.com/2017/09/a-new-article-to-red.html">
```

### HTML 標籤

* [ ] **Language attribute:** ![High][high_img] The `lang` attribute of your website is specified and related to the language of the current page.
* [ ] **Language attribute:** ![High][high_img] 你的網站的 `lang` 屬性被指定以及當前頁面相關語言.

```html
<html lang="en">
```

* [ ] **Direction tag:** ![Medium][medium_img] The direction of lecture is specified on the body tag (It can be used on another HTML tag).
* [ ] **方向標籤:** ![Medium][medium_img]  演講的方向被指定在這個 body 標籤上 (它可以被用來在其他的 HTML 標籤).

```html
<html dir="rtl">
```

> 📖 [dir - HTML - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/dir)

* [ ] **Alternate language:** ![Low][low_img] The language tag of your website is specified and related to the language of the current page.
* [ ] **替代語言:** ![Low][low_img] 你的網站的語言標籤被指定以及相關當前頁面的語言.

```html
<link rel="alternate" href="https://es.example.com/" hreflang="es">
```

* [ ] **Conditional comments:** ![Low][low_img] Conditional comments are present for IE if needed.
* [ ] **條件註解:** ![Low][low_img] 條件註解出現在 IE 如果需要.

> 📖 [關於條件註解 (Internet Explorer) - MSDN - Microsoft](https://msdn.microsoft.com/en-us/library/ms537512(v=vs.85).aspx)

* [ ] **RSS feed:** ![Low][low_img] If your project is a blog or has articles, an RSS link was provided.
* [ ] **RSS 訂閱:** ![Low][low_img] 如果你的專案是部落格或有文章, 一個 RSS 鏈結被提供.

* [ ] **CSS Critical:** ![Medium][medium_img] The CSS critical (or "above the fold") collects all the CSS used to render the visible portion of the page. It is embedded before your principal CSS call and between `<style></style>` in a single line (minified).
* [ ] ** CSS 關鍵:** ![Medium][medium_img] 這個 CSS 關鍵 (或是 "位置明顯") 蒐集所有 CSS 曾經渲染這個頁面的可視部分. 它被嵌入在你的主要的 CSS 呼叫之前 以及 在 `<style></style>` 之間在一行中 (縮小的).

> 🛠 [關鍵由 Addy Osmani 在 Github 上](https://github.com/addyosmani/critical)

* [ ] **CSS order:** ![High][high_img] All CSS files are loaded before any JavaScript files in the `<head>`. (Except the case where sometimes JS files are loaded asynchronously on top of your page).
* [ ] **CSS 順序:** ![High][high_img] 所有 CSS 檔案被裝載在任何 JavaScript 檔案之前在 `<head>` 中. (除了這個例子有時 JS 檔案被非同步地裝載在你的頁面的頂部).

### 社交 meta

***Facebook OG*** and ***Twitter Cards*** are, for any website, highly recommended. The other social media tags can be considered if you target a particular presence on those and want to ensure the display.
***Facebook OG*** 以及 ***Twitter 卡片*** , 對於任何網站, 高度推薦. 其他社交媒體標籤可能被週密考慮過假如你針對特定的存在在那些網站上以及想要確保顯示.

* [ ] **Facebook Open Graph:** ![Low][low_img] All Facebook Open Graph (OG) are tested and no one is missing or with a false information. Images need to be at least 600 x 315 pixels, 1200 x 630 pixels recommended.
* [ ] **Facebook 開放圖表:** ![Low][low_img] 所有 Facebook 開放圖表 (OG) 被檢驗 以及沒一個錯過或是伴隨著一個錯誤資訊. 圖像最少必須是 600 x 315 像素, 1200 x 630 像素被推薦.

```html
<meta property="og:type" content="website">
<meta property="og:url" content="https://example.com/page.html">
<meta property="og:title" content="Content Title">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:description" content="Description Here">
<meta property="og:site_name" content="Site Name">
<meta property="og:locale" content="en_US">
```

> * 📖 [一個導覽分享給網站管理者](https://developers.facebook.com/docs/sharing/webmasters/)
> * 🛠 用這個檢驗你的頁面 [Facebook OG 檢驗](https://developers.facebook.com/tools/debug/)

* [ ] **Twitter Card:** ![Low][low_img]

```html
<meta name="twitter:card" content="summary">
<meta name="twitter:site" content="@site_account">
<meta name="twitter:creator" content="@individual_account">
<meta name="twitter:url" content="https://example.com/page.html">
<meta name="twitter:title" content="Content Title">
<meta name="twitter:description" content="Content description less than 200 characters">
<meta name="twitter:image" content="https://example.com/image.jpg">
```

> * 📖 [用卡片入門 — Twitter Developers](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/guides/getting-started)
> * 🛠 用這個檢驗你的頁面 [Twitter card validator](https://cards-dev.twitter.com/validator)

**[⬆ 回到頂部](#table-of-contents)**

---

## HTML

### 最好的練習

* [ ] **HTML5 Semantic Elements:** ![High][high_img] HTML5 Semantic Elements are used appropriately (header, section, footer, main...).
* [ ] **HTML5 語意元素:** ![High][high_img] HTML5 語意元素使用適當地 (header, section, footer, main...).

> 📖 [HTML 參考](http://htmlreference.io/)

* [ ] **Error pages:** ![High][high_img] Error 404 page and 5xx exist. Remember that the 5xx error page needs to have his CSS integrated (no external call on the current server).
* [ ] **錯誤頁面:** ![High][high_img] 錯誤 404 頁面以及 5xx 存在. 記住 5xx 錯誤頁面必須有他的 CSS 合併 (沒有外部呼叫在正確的伺服器上).

* [ ] **Noopener:** ![Medium][medium_img] In case you are using external links with `target="_blank"`, your link should have a `rel="noopener"` attribute to prevent tab nabbing. If you need to support older versions of Firefox, use `rel="noopener noreferrer"`.
* [ ] **Noopener:** ![Medium][medium_img] 在這個例子你使用外部鏈結伴隨著 `target="_blank"`, 你的鏈結應該有一個 `rel="noopener"` 屬性為了避免 tab 突然抓住. 如果你必須支援火狐的舊版本, 使用 `rel="noopener noreferrer"`.

> 📖 [關於 rel=noopener](https://mathiasbynens.github.io/rel-noopener/)

* [ ] **Clean up comments:** ![Low][low_img] Unnecessary code needs to be removed before sending the page to production.
* [ ] **清理註解:** ![Low][low_img] 不必要的程式碼必須被移除在頁面成為產品前.

### HTML 檢驗

* [ ] **W3C compliant:** ![High][high_img] All pages need to be tested with the W3C validator to identify possible issues in the HTML code.
* [ ] **W3C 兼容:** ![High][high_img] 所有頁面必須被檢驗用這個 W3C 驗證器識別可能議題在這個 HTML 程式碼中.

> 🛠 [W3C 驗證器](https://validator.w3.org/)

* [ ] **HTML Lint:** ![High][high_img] I use tools to help me analyze any issues I could have on my HTML code.
* [ ] **HTML Lint:** ![High][high_img] 我使用工具幫助我分析任何議題我能有在我的 HTML程式碼中.

> 🛠 [骯髒的標記](https://dirtymarkup.com/)

* [ ] **Desktop Browsers:** ![High][high_img] All pages were tested on all current desktop browsers (Safari, Firefox, Chrome, Internet Explorer, EDGE...).
* [ ] **桌面板瀏覽器:** ![High][high_img] 所有頁面被檢驗在所有現在的桌面板瀏覽器 (Safari, Firefox, Chrome, Internet Explorer, EDGE...).
* [ ] **Mobile Browsers:**  ![High][high_img] All pages were tested on all current mobile browsers (Native browser, Chrome, Safari...).
* [ ] **行動版瀏覽器:**  ![High][high_img] 所有頁面被檢驗在所有現在的行動版瀏覽器上 (Native browser, Chrome, Safari...).

* [ ] **Link checker:** ![High][high_img] There are no broken links in my page, verify that you don't have any 404 error.
* [ ] **鏈結檢查:** ![High][high_img] 沒有損壞的鏈結在我的頁面中, 檢驗你沒有任何 404 錯誤.

> 🛠 [W3C 檢查鏈結](https://validator.w3.org/checklink)

* [ ] **Adblockers test:** ![Medium][medium_img] Your website shows your content correctly with adblockers enabled (You can provide a message encouraging people to disable their adblocker).
* [ ] **廣告攔截器檢驗:** ![Medium][medium_img] 你的網站正確顯示你的內容有啟用了廣告攔截器 (你可以提供一個訊息鼓勵人們關閉他們的廣告攔截器).


**[⬆ 回到頂部](#table-of-contents)**

---

## 網頁字體

* [ ] **Webfont format:** ![High][high_img] WOFF, WOFF2 and TTF are supported by all modern browsers.
* [ ] **網頁字體格式:** ![High][high_img] WOFF, WOFF2 以及 TTF 被所有現代瀏覽器支援.

> * 📖 [WOFF - 網頁開放字體格式 - Caniuse](https://caniuse.com/#feat=woff).
> * 📖 [WOFF 2.0 - 網頁開放字體格式 - Caniuse](https://caniuse.com/#feat=woff2).
> * 📖 [TTF/OTF - 理想類型以及開放類型字體支持](https://caniuse.com/#feat=ttf)
> * 📖 [使用 @font-face - CSS-Tricks](https://css-tricks.com/snippets/css/using-font-face/)

* [ ] **Webfont size:** ![High][high_img] Webfont sizes don't exceed 2 MB (all variants included).
* [ ] **網頁字體大小:** ![High][high_img] 網頁字體大小不超過 2 MB (包含所有變型).

**[⬆ 回到頂部](#table-of-contents)**

---

## CSS

> **注意:** 看一眼 [CSS 指南](https://cssguidelin.es/) 以及[Sass 指南](https://sass-guidelin.es/) 跟隨大多數前端開法者. 如果你對 CSS 屬性有疑問, 你可以拜訪 [CSS 參考](http://cssreference.io/).

* [ ] **Responsive Web Design:** ![High][high_img] The website is using responsive web design.
* [ ] **響應式網頁設計:** ![High][high_img] 網頁使用響應式設計.
* [ ] **CSS Print:** ![Medium][medium_img] A print stylesheet is provided and is correct on each page.
* [ ] **CSS 列印:** ![Medium][medium_img] 一個列印樣式表被提供以及正確在每個頁面.
* [ ] **Preprocessors:** ![Medium][medium_img] Your page is using a CSS preprocessor ([Sass](http://sass-lang.com/) is preferred).
* [ ] **預處理器:** ![Medium][medium_img] 你個頁面使用一個 CSS 預處理器 ([Sass](http://sass-lang.com/) 是首選).
* [ ] **Unique ID:** ![High][high_img] If IDs are used, they are unique to a page.
* [ ] **獨一的 ID:** ![High][high_img] 如果 IDs 被使用,它們是一個頁面唯一的.
* [ ] **Reset CSS:** ![High][high_img] A CSS reset (reset, normalize or reboot) is used and up to date. *(If you are using a CSS Framework like Bootstrap or Foundation, a Normalize is already included into it.)*
* [ ] **重置 CSS:** ![High][high_img] 一個 CSS 重置 (reset, normalize or reboot) 被使用而且是最新的. *(如果你使用一個 CSS 框架像 Bootstrap 或是 Foundation, 一個 Normalize 已經被包含進去.)*

> * 📖 [Reset.css](https://meyerweb.com/eric/tools/css/reset/)
> * 📖 [Normalize.css](https://necolas.github.io/normalize.css/)
> * 📖 [Reboot](https://getbootstrap.com/docs/4.0/content/reboot/)

* [ ] **JS prefix:** ![Low][low_img] All classes (or id- used in JavaScript files) begin with **js-** and are not styled into the CSS files.
* [ ] **JS 前綴:** ![Low][low_img] 所有 classes (或是 id- 使用在 JavaScript 檔案中) 首先 **js-** 以及不是進入CSS檔案樣式.

```html
<div id="js-slider" class="my-slider">
<!-- Or -->
<div id="id-used-by-cms" class="js-slider my-slider">
```

* [ ] **CSS embed or line:** ![High][high_img] Avoid at all cost the use of CSS embed or inline: only used for valid reasons (ex: background-image for slider, CSS critical).
* [ ] **CSS 嵌入或行內:** ![High][high_img] 避免所有嵌入或是行內花費: 只用於有效原因 (ex: 背景圖對於 slider, CSS 關鍵).
* [ ] **Vendor prefixes:** ![High][high_img] CSS vendor prefixes are used and are generated accordingly with your browser support compatibility.
* [ ] **供應商前綴:** ![High][high_img] CSS 供應商前綴被使用以及被產生因此伴隨著你的瀏覽器支持兼容性.

> 🛠 [線上自動前綴 CSS](https://autoprefixer.github.io/)

### 效能

- [ ] **Concatenation:** ![High][high_img] CSS files are concatenated in a single file. *(Not for HTTP/2)*
- [ ] **合併:** ![High][high_img] CSS 檔案被合併在一個單一檔案中. *(不適用於 HTTP/2)*
- [ ] **Minification:** ![High][high_img] All CSS files are minified.
- [ ] **縮小:** ![High][high_img] 所有 CSS 檔案被縮小.
- [ ] **Non-blocking:** ![Medium][medium_img] CSS files need to be non-blocking to prevent the DOM from taking time to load.
- [ ] **非阻塞:** ![Medium][medium_img] CSS 檔案必須是非阻塞為了避免 DOM 從花費時間加載.

> * 📖 [讀取 CSS 透過燈絲群組](https://github.com/filamentgroup/loadCSS)
> * 📖 [使用loadCSS預加載CSS的示例](https://gist.github.com/thedaviddias/c24763b82b9991e53928e66a0bafc9bf)

- [ ] **Unused CSS:** ![Low][low_img] Remove unused CSS.
- [ ] **未使用的 CSS:** ![Low][low_img] 刪除未使用的 CSS.

> * 🛠 [UnCSS 線上](https://uncss-online.com/) 🛠
> * 🛠 [PurifyCSS](https://github.com/purifycss/purifycss)
> * 🛠 [Chrome 開發工具覆蓋](https://developers.google.com/web/updates/2017/04/devtools-release-notes#coverage)


### CSS 檢驗

* [ ] **Stylelint:** ![High][high_img] All CSS or SCSS files are without any errors.
* [ ] **Stylelint:** ![High][high_img] 所有 CSS 或是 SCSS 檔案沒有任何錯誤.

> * 🛠 [stylelint, a CSS linter](https://stylelint.io/)
> * 📖 [Sass 指南](https://sass-guidelin.es/)

* [ ] **Responsive web design:** ![High][high_img] All pages were tested at the following breakpoints: 320px, 768px, 1024px (can be more / different according to your analytics).
* [ ] **響應式網頁設計:** ![High][high_img] 所有頁面被檢驗在以下斷點: 320px, 768px, 1024px (根據您的分析可以是更多 / 不同).

* [ ] **CSS Validator:** ![Medium][medium_img] The CSS was tested and pertinent errors were corrected.
* [ ] **CSS 驗證器:** ![Medium][medium_img] 這個 CSS 被檢驗以及相關錯誤得到糾正.

> * 🛠 [CSS 驗證器](https://jigsaw.w3.org/css-validator/)

* [ ] **Desktop Browsers:** ![High][high_img] All pages were tested on all current desktop browsers (Safari, Firefox, Chrome, Internet Explorer, EDGE...).
* [ ] **桌面版瀏覽器:** ![High][high_img] 所有頁面都在當前所有桌面瀏覽器上進行了檢驗 (Safari, Firefox, Chrome, Internet Explorer, EDGE...).
* [ ] **Mobile Browsers:**  ![High][high_img] All pages were tested on all current mobile browsers (Native browser, Chrome, Safari...).
* [ ] **行動版瀏覽器:**  ![High][high_img] 所有頁面都在當前所有的移動瀏覽器上進行檢驗 (Native browser, Chrome, Safari...).
* [ ] **OS:**  ![High][high_img] All pages were tested on all current OS (Windows, Android, iOS, Mac...).
* [ ] **作業系統:**  ![High][high_img] 所有頁面都在當前操作系統上進行了檢驗 (Windows, Android, iOS, Mac...).

- [ ] **Pixel perfect:** ![High][high_img] Pages are close to pixel perfect. Depending on the quality of the creatives, you may not be 100% accurate, but your page needs to be close to your template.
- [ ] **完美像素:** ![High][high_img] 頁面接近完美像素. 取決於創意的品質, 你可能不會 100% 準確, 但你的頁面必須是接近你的模板.

> [完美像素 - Chrome 擴充套件](https://chrome.google.com/webstore/detail/perfectpixel-by-welldonec/dkaagdgjmgdmbnecmcefdhjekcoceebi?hl=en)

* [ ] **Reading direction:** ![High][high_img] All pages need to be tested for LTR and RTL languages if they need to be supported.
* [ ] **閱讀方向:** ![High][high_img] 所有頁面必須檢驗 LTR 和 RTL 語言 假如他們需要被支援.

> * 📖 [建構 RTL-Aware 網頁應用程式 & 網站: 部分 1 - Mozilla Hacks](https://hacks.mozilla.org/2015/09/building-rtl-aware-web-apps-and-websites-part-1/)
> * 📖 [建構 RTL-Aware 網頁應用程式 & 網站: 部分 2 - Mozilla Hacks](https://hacks.mozilla.org/2015/10/building-rtl-aware-web-apps-websites-part-2/)

**[⬆ 回到頂部](#table-of-contents)**

---

## 圖像

> **注意:** 為了圖像優化的完整了解, 檢查免費電子書 **[基本圖像優化](https://images.guide/)** 來自 Addy Osmani.

### 最好的練習

* [ ] **Optimization:** ![High][high_img] All images are optimized to be rendered in the browser. WebP format could be used for critical pages (like Homepage).
* [ ] **優化:** ![High][high_img] 所有圖像都被優化以呈現在瀏覽器中. WebP 格式可用於關鍵頁面 (像首頁).

> * 🛠 [Imagemin](https://github.com/imagemin/imagemin)
> * 🛠 使用 [ImageOptim](https://imageoptim.com/) 免費優化你的圖片.
> * 🛠 使用 [Kraken.io](https://kraken.io/web-interface) 對於 png 和 jpg 優化，使用Kraken.io非常棒的替代方法. 在免費計畫上每個文件最多可達 1 mb .

* [ ] **Picture/Srcset:** ![Medium][medium_img] You use picture/srcset to provide the most appropriate image for the current viewport of the user.
* [ ] **照片/來源設定:** ![Medium][medium_img] 你可以使用照片/來源設定來提供最合適的圖像給用戶的當前視埠.

> * 📖 [如何使用來源設定構建響應式圖像](https://www.sitepoint.com/how-to-build-responsive-images-with-srcset/)

* [ ] **Retina:** ![Low][low_img] You provide layout images 2x or 3x, support retina display.
* [ ] **視網膜:** ![Low][low_img] 您提供 2x 或 3x 的佈局圖像，支持視網膜顯示.
* [ ] **Sprite:** ![Medium][medium_img] Small images are in a sprite file (in the case of icons, they can be in an SVG sprite image).
* [ ] **大圖:** ![Medium][medium_img] 小圖像在一個大圖檔案中 (在圖標的情況下, 他們可以在一個 SVG 大圖圖像中).
* [ ] **Width and Height:** ![High][high_img] Set `width` and `height` attributes on `<img>` if the final rendered image size is known (can be omitted for CSS sizing).
* [ ] **寬度和高度:** ![High][high_img] 設置 `width` 以及 `height` 屬性在 `<img>` 上 假如最終渲染圖像大小被知道 (can be omitted for CSS sizing).
* [ ] **Alternative text:** ![High][high_img] All `<img>` have an alternative text which describe the image visually.
* [ ] **替代文字:** ![High][high_img] 所走 `<img>` 有一個替代文字它直觀地描述了圖像.

> * 📖 [Alt-文字: 終極指南](https://axesslab.com/alt-texts/)

* [ ] **Lazy loading:** ![Medium][medium_img] Images are lazyloaded (A noscript fallback is always provided).
* [ ] **懶加載:** ![Medium][medium_img] 圖像被懶加載 (一個沒有腳本回呼總是被提供).

**[⬆ 回到頂部](#table-of-contents)**

---

## JavaScript

### 最好的練習

* [ ] **JavaScript Inline:** ![High][high_img] You don't have any JavaScript code inline (mixed with your HTML code).
* [ ] **JavaScript 行內:** ![High][high_img] 你沒有任何JavaScript行內代碼(mixed with your HTML code).
* [ ] **Concatenation:** ![High][high_img] JavaScript files are concatenated.
* [ ] **合併:** ![High][high_img] JavaScript 檔案被合併.
* [ ] **Minification:** ![High][high_img] JavaScript files are minified (you can add the `.min` suffix).
* [ ] **縮小:** ![High][high_img] JavaScript 檔案被縮小 (你可以增加 `.min` 後綴).

> * 📖 [縮小支援 (HTML, CSS, and JavaScript)](https://developers.google.com/speed/docs/insights/MinifyResources)

* [ ] **JavaScript 安全性:**

> * 📖 [對於開發安全應用利用 JavaScript 指南](https://www.owasp.org/index.php/DOM_based_XSS_Prevention_Cheat_Sheet#Guidelines_for_Developing_Secure_Applications_Utilizing_JavaScript)

* [ ] **Non-blocking:** ![Medium][medium_img] JavaScript files are loaded asynchronously using `async` or deferred using `defer` attribute.
* [ ] **非阻塞:** ![Medium][medium_img] JavaScript 檔案被讀取非同步地使用 `async` 或是延遲地 `defer` 屬性.

> * 📖 [移除 JavaScript 渲染-阻塞](https://developers.google.com/speed/docs/insights/BlockingJS)

* [ ] **Modernizr:** ![Low][low_img] If you need to target some specific features you can use a custom Modernizr to add classes in your `<html>` tag.
* [ ] **Modernizr:** ![Low][low_img] 如果您需要定位一些特定功能你可以使用一個客製 Modernizr 增加 classes 在你的 `<html>` 標籤中.

> * 🛠 [客製你的 Modernizr ](https://modernizr.com/download?setclasses)

### JavaScript 檢驗

* [ ] **ESLint:** ![High][high_img] ESLint 沒有標記錯誤 (根據您的配置或標準規則).

> * 📖 [ESLint - 用於 JavaScript 和 JSX 的可插拔的 linting 實用程序](https://eslint.org/)

**[⬆ 回到頂部](#table-of-contents)**

---

## 安全

### 掃描並檢查您的網站

> * [securityheaders.io](https://securityheaders.io/)
> * [Observatory by Mozilla](https://observatory.mozilla.org/)
> * [ASafaWeb - ASP.NET 網站的自動安全分析器](https://asafaweb.com/)

### 最好的練習

* [ ] **HTTPS:** ![Medium][medium_img] HTTPS is used on every pages and for all external content (plugins, images...).
* [ ] **HTTPS:** ![Medium][medium_img] 每個頁面都使用 HTTPS 以及適用於所有外部內容 (套件, 圖像...).

> * 🛠 [Let's Encrypt - Free SSL/TLS Certificates](https://letsencrypt.org/)
> * 🛠 [免費 SSL 伺服器測試](https://www.ssllabs.com/ssltest/index.html)
> * 📖 [嚴格的運輸安全](http://caniuse.com/#feat=stricttransportsecurity)

* [ ] **HTTP Strict Transport Security (HSTS):** ![Medium][medium_img] The HTTP header is set to 'Strict-Transport-Security'.
* [ ] **HTTP 嚴格的運輸安全 (HSTS):** ![Medium][medium_img] HTTP 標頭設置為 '嚴格傳輸安全'.

> * 🛠 [檢查 HSTS 預加載狀態和資格](https://hstspreload.org/)
> * 📖 [HTTP 嚴格的運輸安全備忘表 - OWASP](https://www.owasp.org/index.php/HTTP_Strict_Transport_Security_Cheat_Sheet)
> * 📖 [傳輸層保護備忘表 - OWASP](https://www.owasp.org/index.php/Transport_Layer_Protection_Cheat_Sheet)

* [ ] **Cross Site Request Forgery (CSRF):** ![High][high_img] You ensure that requests made to your server-side are legitimate and originate from your website / app to prevent CSRF attacks.
* [ ] **跨站點請求偽造 (CSRF):** ![High][high_img] 您確保向服務器端發出請求是合法的以及來源自你的網站 / 應用程式以防止 CSRF 攻擊.

> * 📖 [跨-網站請求偽造 (CSRF) 預防備忘表  - OWASP](https://www.owasp.org/index.php/Cross-Site_Request_Forgery_(CSRF)_Prevention_Cheat_Sheet)

* [ ] **Cross Site Scripting (XSS):** ![High][high_img] Your page or website is free from XSS possible issues.
* [ ] **跨網站腳本 (XSS):** ![High][high_img] 你的頁面或網站沒有 XSS 的可能議題.

> * 📖 [XSS (跨網站腳本) 預防備忘表  - OWASP](https://www.owasp.org/index.php/XSS_(Cross_Site_Scripting)_Prevention_Cheat_Sheet)
> * 📖 [DOM 基於 XSS 預防備忘表  - OWASP](https://www.owasp.org/index.php/DOM_based_XSS_Prevention_Cheat_Sheet)

* [ ] **Content Type Options** ![Medium][medium_img] Prevents Google Chrome and Internet Explorer from trying to mime-sniff the content-type of a response away from the one being declared by the server.
* [ ] **內容類型選項** ![Medium][medium_img] 防止 Google Chrome 和 Internet Explorer 嘗試模仿-嗅探內容類型遠離服務器聲明的響應.

> * 📖 [X-內容-類型-選項 - Scott Helme](https://scotthelme.co.uk/hardening-your-http-response-headers/#x-content-type-options)

* [ ] **X-Frame-Options (XFO)** ![Medium][medium_img] Protects your visitors against clickjacking attacks.
* [ ] **X-框架-選項 (XFO)** ![Medium][medium_img] 保護你的訪客抵抗點擊劫持攻擊.

> * 📖 [X-框架-選項 - Scott Helme](https://scotthelme.co.uk/hardening-your-http-response-headers/#x-frame-options)
> * 📖 [RFC7034 - HTTP 標頭字段 X-框架-選項](https://tools.ietf.org/html/rfc7034)

* [ ] **Content Security Policy** ![Medium][medium_img] Defines how content is loaded on your site and from where it is permitted to be loaded. Can also be used to protect against clickjacking attacks.
* [ ] **內容安全策略** ![Medium][medium_img] 定義內容如何在你的網站被讀取以及從哪裡被允許加載. 也可以用來防護抵抗點擊劫持攻擊.

> * 📖 [內容安全性策略 - 簡介 - Scott Helme](https://scotthelme.co.uk/content-security-policy-an-introduction/)
> * 📖 [CSP 備忘表 - Scott Helme](https://scotthelme.co.uk/csp-cheat-sheet/)
> * 📖 [CSP 備忘表 - OWASP](https://www.owasp.org/index.php/Content_Security_Policy_Cheat_Sheet)

**[⬆ 回到頂部](#table-of-contents)**

---

## 效能

### 最好的練習

- [ ] **Weight page:** ![High][high_img] The weight of each page is between 0 and 500 KB.
- [ ] **頁面寬度:** ![High][high_img] 每個頁面的寬度介於 0 到 500 KB 之間.

> * 🛠 [網站頁面分析](https://tools.pingdom.com)
> * 📖 [尺寸限制: 使網頁更輕](https://evilmartians.com/chronicles/size-limit-make-the-web-lighter)

- [ ] **縮小:** ![Medium][medium_img] Your HTML is minified.
- [ ] **縮小:** ![Medium][medium_img] 你的 HTML 被縮小.
> * 🛠 [W3C 驗證器](https://validator.w3.org/)

* [ ] **Lazy loading:** ![Medium][medium_img] Images, scripts and CSS need to be lazy loaded to improve the response time of the current page (See details in their respective sections).
* [ ] **懶加載** ![Medium][medium_img] 圖像, 腳本 以及 CSS 必須是懶加載改善反應當前頁面時間(查看細節在他們的各自部分).

* [ ] **Cookie size:** If you are using cookies be sure each cookie doesn't exceed 4096 bytes and your domain name doesn't have more than 20 cookies.
* [ ] **Cookie 大小:** 如果你使用 cookies 確定每個 cookie 不超過 4096 位元組以及你的網域名稱沒有多於 20 個 cookies.

> * 📖 [Cookie 規範: RFC 6265](https://tools.ietf.org/html/rfc6265)
> * 📖 [Cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)
> * 🛠 [瀏覽器 Cookie 限制](http://browsercookielimits.squawky.net/)

* [ ] **Third party components:** ![Medium][medium_img] Third party iframes or components relying on external JS (like sharing buttons) are replaced by static components when possible, thus limiting calls to external APIs and keeping your users activity private.
* [ ] **第三方組件:** ![Medium][medium_img] 第三方内嵌框架或組件依賴在外部 JS 上 (像是分享按紐)在可能的情況下被靜態組件代替, 因此限制呼叫外部 APIs 以及保持你的使用者私人活動.

> * 🛠 [簡單分享按鈕產生器](https://simplesharingbuttons.com/)


### 準備即將到來的請求

> * 📖 [以下技術說明](https://css-tricks.com/prefetching-preloading-prebrowsing/)

* [ ] **DNS resolution:** ![Low][low_img] DNS of third-party services that may be needed are resolved in advance during idle time using `dns-prefetch`.
* [ ] **DNS 決議案:** ![Low][low_img] 第三方服務的 DNS 可能需要提前解決在閒置時間使用 `dns-prefetch` 期間.

```html
<link rel="dns-prefetch" href="https://example.com">
```

* [ ] **Preconnection:** ![Low][low_img] DNS lookup, TCP handshake and TLS negociation with services that will be needed soon is done in advance during idle time using `preconnect`.
* [ ] **預連接:** ![Low][low_img] DNS 查找, TCP 握手以及 TLS 協商與服務這將很快需要提前完成在閒置時間使用 `preconnect` 期間.

```html
<link rel="preconnect" href="https://example.com">
```

* [ ] **Prefetching:** ![Low][low_img] Resources that will be needed soon (e.g. lazy loaded images) are requested in advance during idle time using `prefetch`.
* [ ] **預拿取:** ![Low][low_img] 資源不久將被需要 (e.g. 懶加載圖像)提前被請求在閒置時間使用 `prefetch` 期間.

```html
<link rel="prefetch" href="image.png">
```

* [ ] **Preloading:** ![Low][low_img] Resources needed in the current page (e.g. scripts placed at the end of `<body>`) in advance using `preload`.
* [ ] **預加載:** ![Low][low_img] 資源需要在當前頁面中 (e.g. 腳本放在 `<body>` 的末尾) 在提前使用 `preload` 中.

```html
<link rel="preload" href="app.js">
```

> * 📖 [在預取和預加載之間差異](https://medium.com/reloading/preload-prefetch-and-priorities-in-chrome-776165961bbf)

### 效能檢驗

* [ ] **Google PageSpeed:** ![High][high_img] All your pages were tested (not only the homepage) and have a score of at least 90/100.
* [ ] **Google 頁面速度:** ![High][high_img] 所有你的頁面被檢驗 (不只有首頁) 以及分數最少有 90/100.

> * 🛠 [Google PageSpeed](https://developers.google.com/speed/pagespeed/insights/)
> * 🛠 [用 Google 檢驗你的行動版速度](https://testmysite.withgoogle.com)
> * 🛠 [網站頁面檢測 - 網站效能以及優化檢測](https://www.webpagetest.org/)
> * 🛠 [GTmetrix - 網站速度以及效能優化](https://gtmetrix.com/)

**[⬆ 回到頂部](#table-of-contents)**

---

## 易用性

> **注意:** 你可以觀看播放列表 [A11ycasts with Rob Dodson](https://www.youtube.com/playlist?list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g) 📹

### 最好的練習

- [ ] **Progressive enhancement:** ![Medium][medium_img] Major functionality like main navigation and search should work without JavaScript enabled.
- [ ] **漸進增強:** ![Medium][medium_img] 主要功能像主導航和搜索應該作用沒有啟用 JavaScript .

> * 📖 [啟用 / 不啟用 JavaScript 在 Chrome 開發者工具中](https://www.youtube.com/watch?v=kBmvq2cE0D8)

- [ ] **Color contrast:** ![Medium][medium_img] Color contrast should at least pass WCAG AA (AAA for mobile).
- [ ] **顏色對比:** ![Medium][medium_img] 顏色對比應該最少通過 WCAG AA (AAA for 行動版).

> * 🛠 [對比率](https://leaverou.github.io/contrast-ratio/)

#### 內容標題

* [ ] **H1:** ![High][high_img] All pages have an H1 which is not the title of the website.
* [ ] **H1:** ![High][high_img] 所有頁面有一個 H1 不是網站的標題.
* [ ] **Headings:** ![High][high_img] Headings should be used properly in the right order (H1 to H6).
* [ ] **內容標題:** ![High][high_img] 內容標題應以正確的順序正確使用 (H1 to H6).

> * 📹 [為什麼內容標題以及地標如此重要 -- A11ycasts #18](https://www.youtube.com/watch?v=vAAzdi1xuUY&index=9&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g)

#### 地標

- [ ] **Role banner:** ![High][high_img] `<header>` has `role="banner"`.
- [ ] **旗幟角色:** ![High][high_img] `<header>` 有 `role="banner"`.
- [ ] **Role navigation:** ![High][high_img] `<nav>` has `role="navigation"`.
- [ ] **導航角色:** ![High][high_img] `<nav>` 有 `role="navigation"`.
- [ ] **Role main:** ![High][high_img] `<main>` has `role="main"`.
- [ ] **主要角色:** ![High][high_img] `<main>` has `role="main"`.

> * 📖 [使用 ARIA 路標識別頁面的區域](https://www.w3.org/WAI/GL/wiki/Using_ARIA_landmarks_to_identify_regions_of_a_page)
> * 📖 [ARIA 角色分類](https://www.w3.org/TR/wai-aria/roles#roles_categorization)

### 語義

- [ ] **Specific HTML5 input types are used:** ![Medium][medium_img] This is especially important for mobile devices that show customized keypads and widgets for different types.
- [ ] **具體 HTML5 輸入類型被使用:** ![Medium][medium_img] 這個是特別重要對於行動裝置顯示定制鍵盤以及不同類型的小部件.

> * 📖 [行動版輸入類型](http://mobileinputtypes.com/)

### 表單

* [ ] **Label:** ![High][high_img] A label is associated with each input form element. In case a label can't be displayed, use `aria-label` instead.
* [ ] **Label:** ![High][high_img] 標籤與每個輸入表單元素相關聯. 在案例中標籤無法顯示標籤, 使用 `aria-label` 取代.

> * 📖 [使用 aria-label 屬性 - MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_aria-label_attribute)

### 易用性檢測

* [ ] **Accessibility standards testing:** ![High][high_img] Use the WAVE tool to test if your page respects the accessibility standards.
* [ ] **易用性標準檢測:** ![High][high_img] 使用 WAVE 工具檢測如果你的頁面尊重易用性標準.

> * 🛠 [Wave 檢測](http://wave.webaim.org/)

* [ ] **Keyboard navigation:** ![High][high_img] Test your website using only your keyboard in a previsible order. All interactive elements are reachable and usable.
* [ ] **鍵盤導航:** ![High][high_img] 檢測你的網站僅使用您的鍵盤在可預見的順序中. 所有互動元素都可訪問和可用.
* [ ] **Screen-reader:** ![Medium][medium_img] All pages were tested in a screen-reader (VoiceOver, ChromeVox, NVDA or Lynx).
* [ ] **螢幕-渲染:** ![Medium][medium_img] 所有頁面被檢測在螢幕-渲染中 (VoiceOver, ChromeVox, NVDA or Lynx).
* [ ] **Focus style:** ![High][high_img] If the focus is disabled, it is replaced by visible state in CSS.
* [ ] **焦點樣式:** ![High][high_img] 如果這個焦點被禁用, 它被 CSS 中的可見狀態所取代.

> * 📹 [焦點管理 - A11ycasts #22](https://www.youtube.com/watch?v=srLRSQg6Jgg&index=5&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g)


**[⬆ 回到頂部](#table-of-contents)**

---

## SEO

* [ ] **Google Analytics:** ![High][high_img] Google Analytics is installed and correctly configured.
* [ ] **Google 分析:** ![High][high_img] Google 分析被安裝以及正確地配置.
* [ ] **Headings logic:** ![Medium][medium_img] Heading text helps to understand the content in the current page.
* [ ] **標題邏輯:** ![Medium][medium_img] 標題文字幫助了解內容在當前的頁面中.
* [ ] **sitemap.xml:** ![High][high_img] A sitemap.xml exists and was submitted to Google Search Console (previously Google Webmaster Tools).
* [ ] **sitemap.xml:** ![High][high_img] 一個 sitemap.xml 存在以及被提交給 Google 搜尋控制台 (以前的 Google 網站站長工具).
* [ ] **robots.txt:** ![High][high_img] The robots.txt is not blocking webpages.
* [ ] **robots.txt:** ![High][high_img] 這個 robots.txt 不是阻塞網頁.

> * 🛠 檢驗你的 robots.txt 透過 [Google 機器人檢驗工具](https://www.google.com/webmasters/tools/robots-testing-tool)

* [ ] **Structured Data:** ![High][high_img] Pages using structured data are tested and are without errors. Structured data helps crawlers understand the content in the current page.
* [ ] **結構化數據:** ![High][high_img] 檢驗了使用結構化數據的頁面以及沒有錯誤. 結構化數據幫助爬蟲了解在當前頁面中的內容.

> * 📖 [簡介結構化數據 - 搜尋 - Google 開發者](https://developers.google.com/search/docs/guides/intro-structured-data)
> * 🛠 檢測你的頁面用這個 [結構化數據檢測工具](https://developers.google.com/structured-data/testing-tool/)
> * 🛠 完整的詞彙表可用作結構化數據. [Schema.org Full Heirarchy](http://schema.org/docs/full.html)

* [ ] **Sitemap HTML:** ![Medium][medium_img] An HTML sitemap is provided and is accessible via a link in the footer of your website.
* [ ] **Sitemap HTML:** ![Medium][medium_img] 一個 HTML 網站地圖被提供以及可以訪問通過你的網站的頁尾中的鏈結.

> * 📖 [網站地圖指南 - Google 支援](https://support.google.com/webmasters/answer/183668?hl=en)
> * 🛠 [網站地圖產生器](https://websiteseochecker.com/html-sitemap-generator/)

**[⬆ 回到頂部](#table-of-contents)**

---

## 翻譯

The Front-End Checklist is also available in other languages. Thanks for all translators and their awesome work!
前端檢查清單也提供其他語言版本. 感謝所有的翻譯和他們棒極了的工作

* 🇯🇵 日本: [miya0001/Front-End-Checklist](https://github.com/miya0001/Front-End-Checklist)
* 🇪🇸 西班牙: [eoasakura/Front-End-Checklist-ES](https://github.com/eoasakura/Front-End-Checklist-ES)
* 🇨🇳 中國: [JohnsenZhou/Front-End-Checklist](https://github.com/JohnsenZhou/Front-End-Checklist)
* 🇰🇷 南韓: [kesuskim/Front-End-Checklist](https://github.com/kesuskim/Front-End-Checklist)
* 🇧🇷 葡萄牙文: [jcezarms/Front-End-Checklist](https://github.com/jcezarms/Front-End-Checklist)
* 🇻🇳 越南: [euclid1990/Front-End-Checklist](https://github.com/euclid1990/Front-End-Checklist)
* 🇹🇼 台灣: [EngineLin/Front-End-Checklist](https://github.com/EngineLin/Front-End-Checklist)

---

## 前端檢查清單徽章

If you want to show you are following the rules of the Front-End Checklist, put this badge on your README file!
如果您想顯示您遵循前端檢查清單的規定，請將此徽章放在 README 檔案上！

➔ [![跟隨前端_檢查清單](https://img.shields.io/badge/Front‑End_Checklist-followed-brightgreen.svg)](https://github.com/thedaviddias/Front-End-Checklist/)

```md
[![Front‑End_Checklist followed](https://img.shields.io/badge/Front‑End_Checklist-followed-brightgreen.svg)](https://github.com/thedaviddias/Front-End-Checklist/)
```

**[⬆ 回到頂部](#table-of-contents)**

---

## 貢獻

**Open an issue or a pull request to suggest changes or additions.**
**打開一個議題或是一個拉請求建議改變或是增加.**

### 指南

The **Front-End Checklist** repository consists of two branches:
The **Front-End Checklist** 資料庫由兩個分支組成:

#### 1. `主要的`

This branch consists of the `README.md` file that is automatically reflected on the [Front-End Checklist](http://frontendchecklist.com/) website.
該分支由 `README.md`  文件組成被自動反映在 [前端檢查清單] 網站上(http://frontendchecklist.com/) .

#### 2. `開發`

This branch will be used to make some significant changes to the structure, content if needed. It is preferable to use the master branch to fix small errors or add a new item.
這個分支將被用來做一些重要的事情改變結構, 內容如果需要. 它是優選使用主分支為了修理小錯誤或是增加新項目.

### 貢獻者

Check out all the super awesome [contributors](https://github.com/thedaviddias/frontendchecklist/graphs/contributors).
看看所有超級棒的 [貢獻者](https://github.com/thedaviddias/frontendchecklist/graphs/contributors).

## 支援

If you have any question or suggestion, don't hesitate to use Gitter or Twitter:
如果您有任何問題或建議, 不要猶豫使用 Gitter 或是 Twitter:

* [在 Gitter 上聊天](https://gitter.im/Front-End-Checklist/Lobby?utm_source=share-link&utm_medium=link&utm_campaign=share-link)
* [Facebook](https://www.facebook.com/frontendchecklist/)
* [Twitter](https://twitter.com/thedaviddias)

## 作者

**[David Dias](https://github.com/thedaviddias/Front-End-Checklist)**

## 許可證

[![CC0](https://i.creativecommons.org/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

**[⬆ 回到頂部](#table-of-contents)**

[low_img]: http://res.cloudinary.com/djnyaloac/image/upload/v1508238836/level-checklist-low.png
[medium_img]: http://res.cloudinary.com/djnyaloac/image/upload/v1508238836/level-checklist-medium.png
[high_img]: http://res.cloudinary.com/djnyaloac/image/upload/v1508238836/level-checklist-high.png
