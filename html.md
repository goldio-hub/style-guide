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

<h3>1.4 Multimedia Fallback/h4>
<p dir="rtl">برای داده های چند رسانه ای نسخه های جایگزین فراهم کنید تا درصورتی که محتوا نتوانستند دانلود شوند، جایگزین ها نمایش داده شوند.</p>
<p dir="rtl">برای تصاویر از متن جایگزین با معنایی استفاده کنید. (تگ alt)</p>
<p dir="rtl"></p>
<p dir="rtl"></p>
<p dir="rtl"></p>
<p dir="rtl"></p>
<p dir="rtl"></p>

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
