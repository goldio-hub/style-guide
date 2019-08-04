<h1> CSS Style Guide </h1>

<p dir="rtl">اصولی که در این صفحه مشاهده میکنید، ترکیبی از خط مشی استایل دهی شرکت های بزرگ و تجربه ما میباشد. پیروی از این اصول موجب خوانایی و بالا رفتن کیفیت کار میشود.</p>
<h2 dir="rtl">فهرست</h3>
<ul>
  <li>
    <a href="#1-css-style-rules">1 CSS Style Rules</a>
    <ul>
      <li><a href="#11-id-and-class-naming">1.1 ID and Class Naming</a></li>
      <li><a href="#12-id-and-class-name-style">1.2 ID and Class Name Style</a></li>
      <li><a href="#13-type-selectors">1.3 Type Selectors</a></li>
      <li><a href="#14-shorthand-properties">1.4 Shorthand Properties</a></li>
      <li><a href="#15-0-and-units">1.5 0 and Units</a></li>
      <li><a href="#16-hexdecimal-notation">1.6 Hexdecimal Notation</a></li>
      <li><a href="#17-id-and-class-name-delimiters">1.7 ID and Class Name Delimiters</a></li>
    </ul>
  </li>
  <li>
    <a href="#2-css-formating-rules" >2 CSS Formating Rules</a>
    <ul>
      <li><a href="#2-css-formating-rules">2.1 Declaration Order</a></li>
      <li><a href="#22-block-content-indentation">2.2 Block Content Indentation</a></li>
      <li><a href="#23-declaration-stops">2.3 Declaration Stops</a></li>
      <li><a href="#24-property-name-stops">2.4 Property Name Stops</a></li>
      <li><a href="#25-declaration-block-separation">2.5 Declaration Block Separation</a></li>
      <li><a href="#26-selector-and-declaration-separation">2.6 Selector and Declaration Separation</a></li>
      <li><a href="#27-rule-separation">2.7 Rule Separation</a></li>
      <li><a href="#28-css-quotation-marks">2.8 CSS Quotation Marks</a></li>
    </ul>
  </li>
  <li>
    <a href="#3-css-meta-rules" >3 CSS Meta Rules</a>
      <ul>
        <li><a href="#31-section-comments">3.1 Section Comments</a></li>
        <li><a href="#32-notes">3.2 Notes</a></li>
      </ul>
  </li>
</ul>
<br />
<br />
<h2>1 CSS Style Rules</h2>

<h3>1.1 ID and Class Naming</h4>
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

<br />
<br />

<h3>1.2 ID and Class Name Style</h4>
<p dir="rtl">نام کلاس ها و ID ها باید کوتاه ترین حالت ممکن، ولی به اندازه نیاز بلند باشند. نام کلاس ها باید بتوانند بدون هیچ ابهامی باشند.</p>

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

<br />
<br />

<h3>1.3 Type Selectors</h4>
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

<br />
<br />

<h3>1.4 Shorthand Properties</h4>
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

<br />
<br />

<h3>1.5 0 and Units</h4>
<p dir="rtl">بعد از صفر ها، اگر امکان حذف کردن واحد وجود دارد، واحد را حذف کنید.</p>

#### Good Practice:

```css
flex: 0px; /* نیازمند واحد است flex-basis */
flex: 1 1 0px; /* در اینترنت اکسپلورر 11 به واحد نیاز دارد. */
margin: 0;
padding: 0;
```

<br />
<br />

<h3>1.6 Hexdecimal Notation</h4>
<p dir="rtl">از نمایش 3 تایی هگز در جایی که امکان دارد استفاده کنید. این کار موجب خوانایی بیشتر کد ها میشود. برای مثال زمانی که هر 6 مقداز هگز، دو به دو برابر باشند.</p>

#### Bad Practice:

```css
color: #eebbcc;
```

#### Good Practice:

```css
color: #ebc;
```

<br />
<br />

<h3>1.7 ID and Class Name Delimiters</h4>
<p dir="rtl">از "<bold>-</bold>" برای جدا کردن اسامی کلاس ها و ID ها استفاده کنید.</p>

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

<br />
<br />

<h2>2 CSS Formating Rules</h4>
<p dir="rtl">قوانین قالب CSS</p>


<h3>2.1 Declaration Order</h4>
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
.selector {
  border: 10px solid #333;
  width: 100px;
  height: 100px;
  font-size: 16px;
  padding: 10px;
  margin: 10px;
  position: absolute;
  z-index: 10;
  box-sizing: border-box;
  top: 0;
  right: 0;
  background: #000;
  color: #fff
  font-family: sans-serif;
  font-size: 16px;
  line-height: 1.4;
  overflow: hidden;
  display: inline-block;
  text-align: right;
  cursor: pointer;
}
```

#### Good Practice:

```css
.selector {
  /* Display & Box Model */
  display: inline-block;
  overflow: hidden;
  box-sizing: border-box;
  width: 100px;
  height: 100px;
  padding: 10px;
  border: 10px solid #333;
  margin: 10px;
  
  /* Positioning */
  position: absolute;
  z-index: 10;
  top: 0;
  right: 0;

  /* Color */
  background: #000;
  color: #fff
  
  /* Text */
  font-family: sans-serif;
  font-size: 16px;
  line-height: 1.4;
  text-align: right;

  /* Other */
  cursor: pointer;
}
```

<br />
<br />

<h3>2.2 Block Content Indentation</h4>
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

<br />
<br />

<h3>2.3 Declaration Stops</h4>
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

<br />
<br />

<h3>2.4 Property Name Stops</h4>
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

<br />
<br />

<h3>2.5 Declaration Block Separation</h4>
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

<br />
<br />

<h3>2.6 Selector and Declaration Separation</h4>
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

<br />
<br />

<h3>2.7 Rule Separation</h4>
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

<br />
<br />

<h3>2.8 CSS Quotation Marks</h4>
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

<br />
<br />

<h2>3 CSS Meta Rules</h4>

<h3>3.1 Section Comments</h4>
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

<h3>3.2 Notes</h4>
<ol dir="rtl">
  <li>در استایل دادن ها از ID ها استفاده نکنید.</li>
  <li>در استایل ها از !important استفاده نکنید.</li>
</ol>
