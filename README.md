<h1> CSS Style Guide </h1>

<p dir="rtl"> برای خوانایی بیشتر استایل ها و بیشتر شدن بازدهی کدها، لطفا اصول زیر را رعایت کنید. </p>

<h3 dir="rtl">1.1 ID and Class Naming</h4>
<p dir="rtl">برای نام گذاری اسامی کلاس ها و ID ها ، از کلمات با معنی و مرتبط و کلی استفاده کنید. برای نوشتن کلمات از شیوه نگارش kebab-case استفاده کنید.</p>

#### Bad Practice:

```css
/* Not recommended: meaningless */
#yee-1901 {}

/* Not recommended: presentational */
.button-green {}
.clear {}
```

#### Good Practice:

```css
/* Recommended: specific */
#gallery {}
#login {}
.video {}

/* Recommended: generic */
.aux {}
.alt {}
```

<h3 dir="rtl">1.2 ID and Class Name Style</h4>
<p dir="rtl">نام کلاس ها و ID ها یاید کوتاه ترین حالت ممکن، ولی به اندازه نیاز بلند باشند. نام کلاس ها باید بتوانند بدون هیچ ابهامی باشند.</p>

#### Bad Practice:

```css
#navigation {}
.atr {}
```

#### Good Practice:

```css
#nav {}
.author {}
```

<h3 dir="rtl">1.3 Type Selectors</h4>
<p dir="rtl">تا آنجایی که میتوانید از Type Selector ها استفاده نکنید. به جز زمانی که مجبورید. عدم استفاده از این سلکتور ها، موجب افزایش کارایی می شود. </p>

#### Bad Practice:

```css
ul#example {}
div.error {}
```

#### Good Practice:

```css
#example {}
.error {}
```

<h3 dir="rtl">1.4 Shorthand Properties</h4>
<p dir="rtl">تا آنجایی که امکان دارد، ویژگی ها را کوتاه نگه دارید. این کار باعث خوانایی بیشتر کد، کوتاه شدن کد و افزایش بهره وری می شود.</p>

#### Bad Practice:

```css
border-top-style: none;
font-family: palatino, georgia, serif;
font-size: 100%;
line-height: 1.6;
padding-bottom: 2em;
padding-left: 1em;
padding-right: 1em;
padding-top: 0;
```

#### Good Practice:

```css
border-top: 0;
font: 100%/1.6 palatino, georgia, serif;
padding: 0 1em 2em;
```

<h3 dir="rtl">1.5 0 and Units</h4>
<p dir="rtl">بعد از صفر ها، اگر امکان حذف کردن واحد وجود دارد، واحد را حذف کنید.</p>

#### Good Practice:

```css
flex: 0px; /* نیازمند واحد است flex-basis */
flex: 1 1 0px; /* در اینترنت اکسپلورر 11 به واحد نیاز دارد. */
margin: 0;
padding: 0;
```

<h3 dir="rtl">1.6 Hexdecimal Notation</h4>

<p dir="rtl">از نمایش 3 تایی هگز در جایی که امکان دارد استفاده کنید. این کار موجب خوانایی بیشتر کد ها میشود. برای مثال زمانی که هر 6 مقداز هگز، دو به دو برابر باشند.</p>

#### Bad Practice:

```css
color: #eebbcc;
```

#### Good Practice:

```css
color: #ebc;
```

<h3 dir="rtl">1.7 ID and Class Name Delimiters</h4>
<p dir="rtl">از - برای جدا کردن اسامی کلاس ها و ID ها استفاده کنید.</p>

#### Bad Practice:

```css
/* Not recommended: does not separate the words “demo” and “image” */
.demoimage {}

/* Not recommended: uses underscore instead of hyphen */
.error_status {}
```

#### Good Practice:

```css
/* Recommended */
#video-id {}
.ads-sample {}
```

<h2 dir="rtl">2 CSS Formating Rules</h4>
<p dir="rtl">قوانین قالب CSS</p>


<h3 dir="rtl">2.1 Declaration Order</h4>
<p dir="rtl">ترتیب تعریف ویژگی های هر کلاس CSS باید بر اساس ترتیب زیر باشد.</p>
<ul dir="rtl">
  <li>Display</li>
  <li>Positioning</li>
  <li>Box model</li>
  <li>Colors and Typography</li>
  <li>Other</li>
</ul>

#### Bad Practice:

```css
/* Not recommended: does not separate the words “demo” and “image” */
.demoimage {}

/* Not recommended: uses underscore instead of hyphen */
.error_status {}
```

#### Good Practice:

```css
/* Recommended */
#video-id {}
.ads-sample {}
```

<h3 dir="rtl">2.2 Block Content Indentation</h4>
<p dir="rtl">محتوای هر بلوک باید دارای یک فاصله اضافی باشد. این کار باعث نمایش بهتر سلسه مراتبی میشود.</p>

#### Bad Practice:

```css
@media screen, projection {

html {
  background: #fff;
  color: #444;
}

}
```

#### Good Practice:

```css
@media screen, projection {

  html {
    background: #fff;
    color: #444;
  }

}
```

<h3 dir="rtl">2.3 Declaration Stops</h4>
<p dir="rtl">بعد از هر تعریف، یک ";" قرار دهید. این کار برای انسجام کد بسیار مفید است.</p>

#### Bad Practice:

```css
.test {
  display: block;
  height: 100px
}
```

#### Good Practice:

```css
.test {
  display: block;
  height: 100px;
}
```

<h3 dir="rtl">2.4 Property Name Stops</h4>
<p dir="rtl">بعد از هر ":" یک فاصله قرار دهید.</p>

#### Bad Practice:

```css
h3 {
  font-weight:bold;
}
```

#### Good Practice:

```css
h3 {
  font-weight: bold;
}
```

<h3 dir="rtl">2.5 Declaration Block Separation</h4>
<p dir="rtl">بین آخرین سلکتور و آغاز بلوک از فاصله استفاده کنید</p>
<p dir="rtl">در این قانون، شروع بلوک و آخرین سلکتور باید در یک خط و با یک فاصله از هم قرار داشته باشند.</p>

#### Bad Practice:

```css
/* Not recommended: missing space */
#video{
  margin-top: 1em;
}

/* Not recommended: unnecessary line break */
#video
{
  margin-top: 1em;
}
```

#### Good Practice:

```css
#video {
  margin-top: 1em;
}
```

<h3 dir="rtl">2.6 Selector and Declaration Separation</h4>
<p dir="rtl">برای هر تعریف یا سلکتور، یک خط جدید ایجاد کنید.</p>

#### Bad Practice:

```css
a:focus, a:active {
  position: relative; top: 1px;
}
```

#### Good Practice:

```css
h1,
h2,
h3 {
  font-weight: normal;
  line-height: 1.2;
}
```

<h3 dir="rtl">2.7 Rule Separation</h4>
<p dir="rtl">قوانین را با خط جدید از یکدیگر جدا کنید. هر قانون در خط دوم پس از قانون اول قرار دارد.</p>

#### Bad Practice:

```css
html {
  background: #fff;
}
body {
  margin: auto;
  width: 50%;
}
```

#### Good Practice:

```css
html {
  background: #fff;
}

body {
  margin: auto;
  width: 50%;
}
```

<h3 dir="rtl">2.8 CSS Quotation Marks</h4>
<p dir="rtl">از '' به جای "" در سلکتور های مشخصه ها و مقادیر ویژگی ها استفاده کنید.</p>
<p dir="rtl">از علامت کوتیشن در URI استفاده نکنید</p>
<p dir="rtl">استثناء: اگر نیاز داشتید از @charset استفاده کنید، از "" استفاده کنید، زیرا '' قابل پذیرش در اینجا نیست.</p>

#### Bad Practice:

```css
@import url("https://www.google.com/css/maia.css");

html {
  font-family: "open sans", arial, sans-serif;
}
```

#### Good Practice:

```css
@import url(https://www.google.com/css/maia.css);

html {
  font-family: 'open sans', arial, sans-serif;
}
```

<h3 dir="rtl">3.1 Section Comments</h4>
<p dir="rtl">برای هر بخش یک کامنت توضیحات و جداکننده قرار دهید.</p>

#### Good Practice:

```css
/* Header */

#adw-header {}

/* Footer */

#adw-footer {}

/* Gallery */

.adw-gallery {}
```
