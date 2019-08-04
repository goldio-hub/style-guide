<h1> CSS Style Guide </h1>

<p dir="rtl"> برای خوانایی بیشتر استایل ها و بیشتر شدن بازدهی کدها، لطفا اصول زیر را رعایت کنید. </p>

<h3 dir="rtl">1.1 نام گذاری کلاس و ID</h4>

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

<h3 dir="rtl">1.2 استایل نام گذاری کلاس و ID</h4>

<p dir="rtl">نام کلاس ها و ID ها یاید کوتاه ترین حالت ممکن، ولی به اندازه نیاز بلند باشند. نام کلاس ها باید بتوانند بدون هیچ ابهامی باشند.</p>

#### Bad Practice:

```css
/* Not recommended */
#navigation {}
.atr {}
```

#### Good Practice:

```css
/* Recommended */
#nav {}
.author {}
```

<h3 dir="rtl">1.3 Type Selectors</h4>

<p dir="rtl">تا آنجایی که میتوانید از Type Selector ها استفاده نکنید. به جز زمانی که مجبورید. عدم استفاده از این سلکتور ها، موجب افزایش کارایی می شود. </p>

#### Bad Practice:

```css
/* Not recommended */
ul#example {}
div.error {}
```

#### Good Practice:

```css
/* Recommended */
#example {}
.error {}
```
<h3 dir="rtl">1.4 Shorthand Properties</h4>

<p dir="rtl">تا آنجایی که امکان دارد، ویژگی ها را کوتاه نگه دارید. این کار باعث خوانایی بیشتر کد، کوتاه شدن کد و افزایش بهره وری می شود.</p>

#### Bad Practice:

```css
/* Not recommended */
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
/* Recommended */
border-top: 0;
font: 100%/1.6 palatino, georgia, serif;
padding: 0 1em 2em;
```
