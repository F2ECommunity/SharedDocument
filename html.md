HTML
===
###### tags: `前端(frontend)`,`基礎`,`標籤(tagName)`
-  基礎概念

- 常用標籤介紹

meta 待補
script
link

# 標題

```htmlmixed=
<h1>Good Job!</h1> 
<h2>Good Job!</h1>
<h3>Good Job!</h3>
<h4>Good Job!</h4>
<h5>Good Job!</h5>
<h6>Good Job!</h6>

**有自動換行的效果(<br>)**
```
## Demo

![](https://i.imgur.com/rsL4PZn.jpg)


# 段落
```htmlmixed=
<p>段落標籤，會自己換行</p>


**有自動換行的效果(<br>)**
```

## Demo

![](https://i.imgur.com/xJMwb2I.jpg)


# 粗體

```htmlmixed=
<strong>將文字加粗</strong>
<b>同樣將文字加粗</b>

<strong>和<b>標籤結果相同和使用意義不同
<strong>偏向關鍵字，<b>偏向該注意的段落
```

## Demo

![](https://i.imgur.com/RFJFvTb.png)





# 斜體

```htmlmixed=
<i>貓咪</i>
<em>狗狗</em>

<i>和<em>效果相同但意義不同
<i>   常用在術語，諺語，專有名詞等
<em>  強調語意
```

## Demo

![](https://i.imgur.com/jDLUhGH.jpg)

# 螢光筆標記

```htmlmixed=
<mark>同學們這題會考，請記住</mark>
```

## Demo

![](https://i.imgur.com/XwVZ17b.png)


# 字體大小

```htmlmixed=
<small>大</small>
<big>小</big>
```

## Demo

![](https://i.imgur.com/URWCPYZ.png)

# 預先格式化

```htmlmixed=

<pre>
將文件的 空白
換行完整呈現
</pre>

```

## Demo

![](https://i.imgur.com/qIUrQSg.png)



# 刪除線

```htmlmixed=
<del>你看不到我</del>
```

## Demo

![](https://i.imgur.com/Tc5DXf7.png)


# 底線

```htmlmixed=
<ins>我從陰影中到來</ins>
```

## Demo

![](https://i.imgur.com/qvN5tJ9.png)

# 上下標標籤

```htmlmixed=
10<sup>2</sup>

<sub>2</sub>10
```

## Demo

![](https://i.imgur.com/5eetmzR.png)


# 區塊引用

```htmlmixed=
<blockquote>文字會往內縮排</blockquote>

```

## Demo

![](https://i.imgur.com/wFNcV3z.png)


# 縮寫
```htmlmixed=
<abbr title="一個表記表示這是縮寫，一定要配合title屬性使用">縮寫</abbr>

title 屬性當滑鼠在該標籤上面，會出現title內的說明文字
```

## Demo

![](https://i.imgur.com/ZwXZ7Pw.png)


# 雙引號

```htmlmixed=
<q>我是誰，我在哪</q>
```

## Demo

![](https://i.imgur.com/5zx4WfO.png)


# 地址

```htmlmixed=
<address>薩里郡小惠因區水蠟樹街4號，樓梯下的碗櫥</address>
```

## Demo

![](https://i.imgur.com/0FEqcnq.png)


# 作品

```htmlmixed=
<cite>我思故我在</cite>
```

## Demo

![](https://i.imgur.com/L0ymPEh.png)


# 文字反轉

```htmlmixed=
<bdo dir="rtl">醫學證明，文字組合不影響閱讀順序</bdo>

dir 屬性
    rtl 反轉文字
    ltr 正常顯示

```

## Demo

![](https://i.imgur.com/lomFUXa.png)


# 超連結

```htmlmixed=
<a href="http://www.youtube.com" target="_blank">Youtube</a> 超連結


target 屬性
    _self，同樣的網頁跳轉
    _blank，開一個新的分頁
    _top，將本身的分割視窗頁關閉，並在原處開啟一個單面的網頁
    _parent，效果與_self相同
```

## Demo

![](https://i.imgur.com/4f6UvjM.png)



# 圖片

```htmlmixed=
<img src="html5.jpeg" alt="HTML5 Icon">

屬性說明
src (檔案來源/路徑)
alt (找不到檔案，出現的替代文字)

```
<font style="color:orangered;">備註:會推薦使用css，屬性來控制長寬</font>

## Demo

![](https://i.imgur.com/pSsAYzh.png)


# 表格

```htmlmixed=
範例一

<table>
    <caption>資料表A</caption>
    <tr>
        <th>欄位A</th>
        <th>欄位B</th>
    </tr>
    <tr>
      <td>資料1</td>
      <td>資料2</td>
    </tr>
</table>

  

範例二

<table>
    <caption>死亡名單</caption>
    <colgroup>
     <col span="2" style="background-color:blue">
     <col style="background-color:purple">
    </colgroup>
    <thead>
      <tr>
        <td>姓名</td>
        <td>死因</td>
        <td>地點</td>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>江戶川</td>
        <td>窒息</td>
        <td>辦公室</td>
      </tr>
    </tbody>
    <tfoot>
      <tr>
        <td>金田一</td>
        <td>中毒</td>
        <td>廚房</td>
      </tr>
    </tfoot>
</table>

標籤說明
caption    表格上方的標題
th         表格內首行(加粗)
tr         列
td         行
thead      整段首行(內元素套上th的效果)
tbody      標籤無效果
tfoot      標籤無效果
colgroup   行 css批次設定

屬性說明
rowspan    併列
colspan    併行

```

<font style="color:orangered;">備註:樣式使用CSS來裝飾，不建議使用html5以前的標籤屬性</font>

## Demo

範例一

![](https://i.imgur.com/ianAoIq.png)

範例二

![](https://i.imgur.com/63EVB0M.png)


# 列表

```htmlmixed=
<ul>
    <li>我的就是我的</li>
    <li>你的就是我的</li>
    <li>他的就是我的</li>
    <li>全部就是我的</li>
</ul>

<ol>
    <li>一口</li>
    <li>兩口</li>
</ol>

<dl>
    <dt>購買清單</dt>
    <dd>胡蘿蔔</dd>
</dl>
  
  
標籤說明
ol有序 
ul無序 li項目
dl清單 dt項目 dd描述

```

## Demo

![](https://i.imgur.com/DmOaLBj.png)

![](https://i.imgur.com/ifqEuWc.png)

![](https://i.imgur.com/9wtUiCd.png)


# 表單

```htmlmixed=

範例一

<form action="" method="post" target="">
    <label for="lname">大名:</label>
    <input type="text" size="6" maxlength="5"><br>
    <input type="submit" value="送出">
</form>

標籤說明

label 文字標籤


屬性
    action      送到的頁面
    for         label限定的id
    method      表單送出的方法GET或POST
    type        定義input型別，根據型別可輸入各種值
    size        輸入框的長度
    maxlength   輸入框字數限制 
    
```

![](https://i.imgur.com/NrYvL8m.png)


```htmlmixed=
範例二


<form action="" method="post">
    <label for="fruit">水果:</label>
    <select>
      <option value="straw">草莓</option>
      <option value="bana">香蕉</option>
      <option value="lem">檸檬</option>
      <option value="pine">鳳梨</option>
    </select><br>
    <input type="submit" value="送出">
</form>

標籤說明:
  select   選單 
  option   選項

```

![](https://i.imgur.com/D3PtMVa.png)


```htmlmixed=
範例三

<form class="" action="index.html" method="post">
 
    <label for="question_weapon">你想攜帶哪種武器?</label>
    <input type="radio" id="dosabow" name="equips" value="dosabow">
    <label for="dosabow">謊言豆沙包</label>
    <input type="radio" id="lolipop" name="equips" value="lolipop">
    <label for="lolipop">慚愧棒棒糖</label><br>
    
    <label for="question_deal">你想吃哪幾餐?</label>
    <input type="checkbox" name="breakfast" value="breakfast">
    <label for="Bike">早餐</label>
    <input type="checkbox" name="lunch" value="lunch">
    <label for="Bike">晚餐</label>
    <input type="checkbox" name="dinner" value="dinner">
    <label for="Bike">晚餐</label><br>
    
    <input type="submit" value="送出">
    
</form>

當input的type屬性為radio時，是用name當作是否為同一組選項

```

![](https://i.imgur.com/SSnO8J9.png)


```htmlmixed=
範例四

<form class="" action="" method="post">
    <input type="month" id="bdaymonth" name="bdaymonth"><br>
    <input type="week" id="week" name="week"><br>
    <input type="time" id="appt" name="appt"><br>
    <input type="tel" id="phone" name="phone" pattern="[0-9]{3}-[0-9]{2}-[0-9]{3}"><br>
    <input type="submit" value="送出">
</form>

屬性 
 pattern 限制輸入格式

```

![](https://i.imgur.com/mRAQacf.png)


```htmlmixed=
範例五

<form class="" action="index.html" method="post">
    <input type="number" id="quantity" name="quantity" min="1" max="5"><br>
    <input type="search" id="gsearch" name="gsearch"><br>
    <textarea name="name" rows="8" cols="80"></textarea><br>
    <input type="button" value="按我">
    <input type="submit" value="送出">
</form>

標籤
textarea  複行輸入框

屬性
  cols, rows 設定textarea文字框的預設大小
  min, max 控制數字輸入框右方上下bar的上限

```

![](https://i.imgur.com/J4QLBFa.png)


```htmlmixed=
範例六

  <form class="" action="index.html" method="post" target="">
    <label for="files">Select files:</label><br/>
    <input type="file" id="upfile" name="upfile">
    <label for="files">Select files:</label><br/>
    <input type="file" id="upfiles" name="upfiles" multiple>
    <input type="submit" value="送出">
  </form>
  
  
  屬性:
   multiple 複選檔案上傳

```

![](https://i.imgur.com/MTtRXWD.jpg)



```htmlmixed=
範例七

    <input type="text" id="username" name="username" required><br>
    <input type="text" name="fname" autofocus><br>
    <input type="text" readonly><br>
    <input type="text" placeholder="請輸入"><br>

    
    <br><br>
    
    <input list="browsers">
    <datalist id="browsers">
    <option value="Internet Explorer">
    <option value="Firefox">
    </datalist>

    補充 
    1.input type="button" 和 button標籤雖然效果相同但由於button標籤在不同瀏覽器會產生不同效果
    因此會建議使用 input標籤來生成按鈕
    2.補充的標籤 formaction formenctype formmethod formtarget formnovalidate novalidate 不常用但可以嘗試
    使用看看效果如何

    標籤
    datalist 需要和input 並使用list搭配使用，可以做出下拉式選單的效果

    
    屬性 
    (加在標籤中即可)
    readonly    此欄位只能顯示無法輸入
    required    此欄為必填欄位
    disabled    在網頁看不到此欄也無法使用
    autofocus   載入網頁輸入提示會顯示在此欄位上

    正常使用的
    placeholder input欄位未有值的提示文字

```
![](https://i.imgur.com/9knRHMC.png)


# <font style="color:blue;">導覽列</font>

```htmlmixed=
<nav>
    <a style="color:whitesmoke" href="1">首頁</a>
    <a style="color:whitesmoke" href="2">內容</a>
    <a style="color:whitesmoke" href="3">協作</a>
    <a style="color:whitesmoke" href="4">關於我</a>
</nav>

用於定義導覽列區塊
```

## Demo

![](https://i.imgur.com/gButqQT.png)


# 區塊

```htmlmixed=
區塊只是方便讓你調整css屬性或者控制某段畫面一起調整，沒有其他效果

<header></header>
<div></div>
<main></main>
<Section></Section>
<article></article>
<aside></aside>
<footer></footer>
```


# 內行

```htmlmixed=
如果你只有某行程式需要效果可以使用這個標籤

<span style="color:red;">您真內行?</span>

```

## Demo

![](https://i.imgur.com/0a0jSN6.png)





# 其他單行標籤

```htmlmixed=
<span>喔</span>
<span>喔齁齁</span><br>
<span>喔齁齁齁</span>
<hr>
<span>哈哈哈哈</span>

```

## Demo

![](https://i.imgur.com/9YEzzeU.png)


# 其他特殊用途標籤

```htmlmixed=
<noscript>當客戶端不支援或是禁用 JavaScript時，會將標籤內容會顯示出來。</noscript>

<code>標記為程式碼</code>


time中的datetime屬性會自動被轉化機器可讀的格式，共兩個用途
1.瀏覽器可以透過使用者的行事曆來增加日期提醒
2.搜尋引擎能找出更正確的結果
<time datetime="2008-02-14"></time>

<var>標記為程式變數或數學表達式，斜體效果</var>

<samp>標記為程式輸出結果，效果為字形會是瀏覽器的monospace字體</samp>


**補充說明:這邊的標籤平時很少使用，看自己的開發習慣來使用就好**

```


## Demo

![](https://i.imgur.com/f0T4fXj.png)


# 額外補充資料
1. [html特殊符號對照表](https://codertw.com/%E7%A8%8B%E5%BC%8F%E8%AA%9E%E8%A8%80/533294/)

# 文件參考資料
1. [w3school](https://www.w3schools.com/)
2. [wibibi教學百科](https://www.wibibi.com/)


