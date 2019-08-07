# HTML Style Guide

<p dir="rtl">اصولی که در این صفحه مشاهده میکنید، ترکیبی از خط مشی استایل دهی شرکت های بزرگ و تجربه ما میباشد. پیروی از این اصول موجب خوانایی و بالا رفتن کیفیت کار میشود.</p>

<h2 dir="rtl"> فهرست </h2>

<ul>
  <li>
    <a href="#1-html-style-rules">1 HTML Style Rules</a>
    <ul>
      <li><a href="#11-document-type">1.1 Document Type</a></li>
      <li><a href="#12-html-validity">1.2 HTML Validity</a></li>
      <li><a href="#13-semantics">1.3 Semantics</a></li>
      <li><a href="#14-multimedia-fallback">1.4 Multimedia Fallback</a></li>
      <li><a href="#15-separation-of-concerns">1.5 Separation of Concerns</a></li>
      <li><a href="#16-entity-references">1.6 Entity References</a></li>
      <li><a href="#17-type-attributes">1.7 <code>type</code> Attributes</a></li>
      <li><a href="#18-meta-data">1.8 Meta Data</a></li>
      <li><a href="#19-setting-the-viewport">1.9 Setting The Viewport</a></li>
    </ul>
  </li>
  <li>
    <a href="#2-html-formatting-rules">2 HTML Formatting Rules</a>
    <ul>
      <li><a href="#21-general-formatting">2.1 General Formatting</a></li>
      <li><a href="#22-html-line-wrapping">2.2 HTML Line-Wrapping</a></li>
      <li><a href="#23-html-quotation-marks">2.3 HTML Quotation Marks</a></li>
      <li><a href="#24-html-closing-tags">2.4 HTML Closing Tags</a></li>
      <li><a href="#25-html-spaces-and-equal-signs">2.5 HTML Spaces and Equal Signs</a></li>
    </ul>
  </li>
</ul>

<br />
<br />

## 1 HTML Style Rules

### 1.1 Document Type
<p dir="rtl">از HTML5 استفاده کنید</p>
<p dir="rtl">حتما از تگ <code>&#60;!DOCTYPE html&#62;</code> در اول فایل خود استفاده کنید تا مشخص شود از استاندارد چه html ای استفاده میکنید.</p>
<p dir="rtl">برای تمام تگ هایی که نیازی به بسته شدن ندارند نیز تگ بسته را قرار دهید.</p>

#### Bad:

```html
<img src="source" alt="alternative" >
```

#### Good:

```html
<img src="source" alt="alternative" />
```

<br />
<br />

### 1.2 HTML Validity
<p dir="rtl">همیشه از HTML های معتبر استفاده کنید.</p>
<p dir="rtl">تنها درصورتی که نیاز به افزایش کارایی سیستم با استفاده از کم کردن حجم فایل ها دارید، حق دارید این قانون را عمل نکنید که البته این کار باید توسط ابزار ها و در فایل دیگری صورت بگیرد و برنامه نویسان همیشه موظف به رعایت این قانون هستند.</p>
<p dir="rtl">از ابزارهایی مثل <a href="https://validator.w3.org/">W3 HTML validator</a> برای تست کردن صحت کد های خوداستفاده کنید.</p>

#### Bad:

```html
<title>Test</title>
<article>This is only a test.
```

#### Good:

```html
<!DOCTYPE html>
<meta charset="utf-8">
<title>Test</title>
<article>This is only a test.</article>
```

<br />
<br />

### 1.3 Semantics
<p dir="rtl">از تگ های HTML با توجه به هدفشان استفاده کنید.</p>
<p dir="rtl">تگ های HTML هر یک دارای یک هدفی هستند که در حین توسعه آن ها در نظر گرفته شده اند.</p>
  <p dir="rtl">برای مثال برای پاراگراف ها از تگ <code>p</code> و برای سرتیتر ها از تگ <code>h</code> و برای دکمه ها از تگ <code>button</code> استفاده کنید.</p>
<p dir="rtl">استفاده درست از تگ های HTML موجب بالا رفتن کارایی و خوانایی بهتر کد و دسترسی بهتر برای افراد ناتوان میشود.</p>

#### Bad:

```html
<div onclick="goToRecommendations();">All recommendations</div>
```

#### Good:

```html
<a href="recommendations/">All recommendations</a>
```

<br />
<br />

### 1.4 Multimedia Fallback
<p dir="rtl">برای داده های چند رسانه ای نسخه های جایگزین فراهم کنید تا درصورتی که محتوا نتوانستند دانلود شوند، جایگزین ها نمایش داده شوند.</p>
<p dir="rtl">برای تصاویر از متن جایگزین با معنایی استفاده کنید. (تگ alt)</p>
<p dir="rtl">برای ویدیو ها و صوت ها کپشن قرار دهید و درصورت امکان متن صوت و ویدیو را نیز در ترنسکریپت آن قرار دهید.</p>
<p dir="rtl">فراهم کردن محتوای ثانویه، برای قابلیت دستری افراد ناتوان بسیار مهم است. برای مثال برای فرد نابینا، اگر این محتوای جایگزین وجود نداشته باشد، فهمیدن اینکه این بخش سایت چه چیزی وجود دارد و برای چه وجود دارد غیر قابل فهم میشود.</p>
<p dir="rtl">برای تصاویری که تنها هدف آن ها دیزاین سایت است و نمیتوان برای آن ها محتوای جایگزینی پیدا کرد، میتوان از رشته خالی برای محتوای جایگزین استفاده کرد.</p>

#### Bad:

```html
<img src="spreadsheet.png">
```

#### Good:

```html
<img src="spreadsheet.png" alt="Spreadsheet screenshot.">
```

<br />
<br />

### 1.5 Separation of Concerns
<p dir="rtl">رفتار، ظاهر و ساختار را همیشه جدا از هم نگه دارید.</p>
<p dir="rtl">تا جایی که میتوانید فایل های ساختاری HTML فایل های رفتاری scripts و فایل های ظاهری styling را از یکدیگر جدا نگه دارید.</p>
<p dir="rtl">این کار به خاطر نگه داری بهتر انجام میشود. تغییر یک استایل در فایل styles راحت تر از تغییر آن در template اصلی میباشد.</p>

#### Bad:

```html
<!DOCTYPE html>
<title>HTML sucks</title>
<link rel="stylesheet" href="base.css" media="screen">
<link rel="stylesheet" href="grid.css" media="screen">
<link rel="stylesheet" href="print.css" media="print">
<h1 style="font-size: 1em;">HTML sucks</h1>
<p>I’ve read about this on a few sites but now I’m sure:
  <u>HTML is stupid!!1</u>
<center>I can’t believe there’s no way to control the styling of
  my website without doing everything all over again!</center>
```

#### Good:

```html
<!DOCTYPE html>
<title>My first CSS-only redesign</title>
<link rel="stylesheet" href="default.css">
<h1>My first CSS-only redesign</h1>
<p>I’ve read about this on a few sites but today I’m actually
  doing it: separating concerns and avoiding anything in the HTML of
  my website that is presentational.
<p>It’s awesome!
```

<br />
<br />

### 1.6 Entity References
<p dir="rtl">از علامت هایی مثل <code>&amp;mdash;</code> استفاده نکنید. و به جای آن از کاراکتر های UTF-8 استفاده کنید. </p>
<p dir="rtl">تنها برای کارکتر های ویژه مانند نیم فاصله مجاز به استفاده از این کارکتر ها هستید.</p>

#### Bad:

```html
The currency symbol for the Euro is &ldquo;&eur;&rdquo;.
```

#### Good:

```html
The currency symbol for the Euro is “€”.
```

<br />
<br />

### 1.7 <code>type</code> Attributes
<p dir="rtl">برای stylesheet ها و script ها، <code>type</code> را حذف نمایید.</p>
<p dir="rtl">از <code>type</code> استفاده نکنید، مگر اینکه جیزی غیر از css و یا javascript باشد.</p>
<p dir="rtl">وقتی <code>type</code> را حذف میکنیم، به طور خودکار مرورگرها این موارو را با مقدار پیشفرض مشخص میکنند.</p>

#### Bad:

```html
<link rel="stylesheet" href="https://www.google.com/css/maia.css" type="text/css">

<script src="https://www.google.com/js/gweb/analytics/autotrack.js" type="text/javascript"></script>
```

#### Good:

```html
<link rel="stylesheet" href="https://www.google.com/css/maia.css">

<script src="https://www.google.com/js/gweb/analytics/autotrack.js"></script>
```

<br />
<br />

### 1.8 Meta Data
<p dir="rtl">تگ عنوان، در HTML5 ضروری است و نمیتوان آن را حذف کرد.</p>
<p dir="rtl">سعی کنید تا برای هر صفحه با معنی ترین عنوان ممکن را انتخاب کنید.</p>
<p dir="rtl">برای اطمینان حاصل کردن از دیده شدن توسط موتور های جستجو، حتما زبان و کاراکتر را در سند مشخص کنید.</p>

#### Good:

```html
<!DOCTYPE html>
<html lang="en-US">
<head>
  <meta charset="UTF-8">
  <title>HTML5 Syntax and Coding Style</title>
</head>
```

<br />
<br />

### 1.9 Setting The Viewport
<p dir="rtl">قسمتی از صفحه وب که توسط کاربر دیده میشود، Viewport نام دارد که میتوان از طریق تگ <code>meta</code> آن را کنترل کرد.</p>
<p dir="rtl">این تگ برای مرورگر دستوراتی را فراهم میکند که باعث میشود ابعاد و مقیاس در گوشی متفاوت با کامپیوتر دیده شود.</p>
<p dir="rtl">میتوانید تفاوت وجود و عدم وجود این تگ را در <a href="https://www.w3schools.com/css/css_rwd_viewport.asp">اینجا</a> مشاهده کنید.</p>

#### Good:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

<br />
<br />

## 2 HTML Formatting Rules

### 2.1 General Formatting
<p dir="rtl">برای هر فرزند بلوک، لیست یا عنصر جدول، یک خط جدید ایجاد کنید.</p>
<p dir="rtl">برای هر فرزند هر بلوک، یک فرو رفتگی ایجاد کنید.</p>
<p dir="rtl">تنها برای آیتم های لیست ها میتوانید درصورتی که فقط دارای متن بودند، در یک خط قرار دهید.</p>
<p dir="rtl">هر فرورفتگی باید شامل 2 فاصله باشد.</p>
<p dir="rtl">از تب برای فرو رفتگی ها استفاده نکنید.</p>
<p dir="rtl">تمام حروف تگ ها و ویژگی ها باید حروف کوچک باشند.</p>
<p dir="rtl">در پایان خط ها فاصله ایجاد نکنید.</p>

#### Bad:

```html
<SECTION> 
  <p>This is a paragraph.</p>
</SECTION>
```

```html
<Section> 
  <p>This is a paragraph.</p>
</SECTION>
```

```html
<div CLASS="menu">
```

#### Good:

```html
<section> 
  <p>This is a paragraph.</p>
</section>
```

```html
<div class="menu">
```

```html
<blockquote>
  <p><em>Space</em>, the final frontier.</p>
</blockquote>
```

```html
<ul>
  <li>Moe</li>
  <li>Larry</li>
  <li>Curly</li>
</ul>
```

```html
<table>
  <thead>
    <tr>
      <th scope="col">Income</th>
      <th scope="col">Taxes</th>
  <tbody>
    <tr>
      <td>$ 5.00</td>
      <td>$ 4.50</td>
</table>
```
<br />
<br />

### 2.2 HTML Line-Wrapping
<p dir="rtl">خط های بلند را بشکانید.</p>
<p dir="rtl">اگرجه برای HTML درمورد طول هر سطر موردی بیان نشده، اما درصورتی که طول خط بسیار بلند شد و شکستن خط موجب بالارفتن خوانایی میشد، خط را بشکانید.</p>

#### Bad:

```html
<md-progress-circular md-mode="indeterminate" class="md-accent"
    ng-show="ctrl.loading" md-diameter="35">
</md-progress-circular>
```

```html
<md-progress-circular md-mode="indeterminate"
                      class="md-accent"
                      ng-show="ctrl.loading"
                      md-diameter="35">
</md-progress-circular>
```

#### Good:

```html
<md-progress-circular
    md-mode="indeterminate"
    class="md-accent"
    ng-show="ctrl.loading"
    md-diameter="35">
</md-progress-circular>
```

<br />
<br />

### 2.3 HTML Quotation Marks
<p dir="rtl">از دابل کوتیشن <code>" "</code> برای مقدار دهی ویژگی ها استفاده کنید.</p>

#### Bad:

```html
<table class=table striped>
```

```html
<table class=striped>
```

```html
<a class='maia-button maia-button-secondary'>Sign in</a>
```

#### Good:

```html
<a class="maia-button maia-button-secondary">Sign in</a>
```

```html
<table class="striped">
```

<br />
<br />

### 2.4 HTML Closing Tags
<p dir="rtl">همیشه تمامی تگ ها را ببندید.</p>

#### Bad:

```html
<meta charset="utf-8">
```

```html
<section>
  <p>This is a paragraph.
  <p>This is a paragraph.
</section>
```

#### Good:

```html
<meta charset="utf-8" />
```

```html
<section>
  <p>This is a paragraph.</p>
  <p>This is a paragraph.</p>
</section>
```

<br />
<br />

### 2.5 HTML Spaces and Equal Signs
<p dir="rtl">از فاصله دادن بین علامت مساوی و ویژگی ها پرهیز کنید.</p>

#### Bad:

```html
<link rel = "stylesheet" href = "styles.css">
```

#### Good:

```html
<link rel="stylesheet" href="styles.css">
```

<br />
<br />
