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
