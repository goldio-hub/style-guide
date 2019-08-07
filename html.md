# HTML Style Guide

<p dir="rtl">اصولی که در این صفحه مشاهده میکنید، ترکیبی از خط مشی استایل دهی شرکت های بزرگ و تجربه ما میباشد. پیروی از این اصول موجب خوانایی و بالا رفتن کیفیت کار میشود.</p>
<h2 dir="rtl">فهرست</h3>
<ul>
  <li>
    <a href="#1-html-style-rules">1 HTML Style Rules</a>
    <ul>
      <li><a href="#11-id-and-class-naming">1.1 Document Type</a></li>
    </ul>
  </li>
  <li>
    <a href="" ></a>
    <ul>
      <li><a href=""></a></li>
    </ul>
  </li>
</ul>

<br />
<br />

<h2>1 HTML Style Rules</h2>

<h3>1.1 Document Type</h4>
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

<h3>1.2 HTML Validity</h4>
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

<h3>1.3 Semantics/h4>
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

<h3>1.4 Multimedia Fallback </h4>
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

<h3>1.5 Separation of Concerns</h4>
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

<h3>1.6 Entity References</h4>
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

<h3>1.7 <code>type</code> Attributes</h4>
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

<h2>2 HTML Formatting Rules</h2>

<h3>2.1 General Formatting</h4>
<p dir="rtl">برای هر فرزند بلوک، لیست یا عنصر جدول، یک خط جدید ایجاد کنید.</p>
<p dir="rtl">برای هر فرزند هر بلوک، یک فرو رفتگی ایجاد کنید.</p>
<p dir="rtl">تنها برای آیتم های لیست ها میتوانید درصورتی که فقط دارای متن بودند، در یک خط قرار دهید.</p>

#### Good:

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

<h3>2.2 HTML Line-Wrapping</h4>
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

<h3>2.3 HTML Quotation Marks</h4>
<p dir="rtl">از دابل کوتیشن <code>" "</code> برای مقدار دهی ویژگی ها استفاده کنید.</p>

#### Bad:

```html
<a class='maia-button maia-button-secondary'>Sign in</a>
```

#### Good:

```html
<a class="maia-button maia-button-secondary">Sign in</a>
```

<br />
<br />
