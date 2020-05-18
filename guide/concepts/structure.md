---
title: ساختار فایل ها 
prev: ../
next: ./layouts
---

## assets
این پوشه شامل فایل های کامپایل نشده ی پروژه می باشد. برای مثال فایل های Sass و less در این پوشه قرار می گیرند.

## components
این پوشه مخصوص قرار دادن کامپوننت های ویو جی اس می باشد. از متد asyncData در کامپوننت ها نمی توان استفاده کرد. بهتر است نام کامپوننت ها هماهنگ با نام صفحات در فولدر های مشخص قرار داده شود تا دستیابی به یک کامپوننت خاص آسان تر باشد.

## layouts
فولدر لیوت مخصوص قرار دادن فایل های لیوت پروژه می باشد. این فولدر به هیچ وجه قابل تغییر نیست. لیوت ها لایه های ثابت صفحه می باشند (مانند سایدبار).
 
## middleware
در این فولدر میدلویر ها قرار می گیرند. میدل ویرها قبل از اجرای و یا تغییر صفحات اجرا می شوند.
 
## pages
شاید مهمترین فولدر ناکس همین باشد. در این فولدر صفحات با فرمت vue. قرار میگیرند و متناسب با فولدرها و فایل ها روتینگ ناکس شکل می گیرد. 

| فایل        | برابر است با           | 
| ------------- |:-------------:| 
| pages/user/profile.vue      | http://site.com/user/profile | 

## static
فایل های غیرقابل تغییر که قابلیت دانلود مسقیم دارند در این فولدر قرار می گیرند. این فولدر را نمی توان تغییر نام داد. برای مثال
| فایل        | برابر است با           | 
| ------------- |:-------------:| 
| /static/favicon.ico       | https://site.com/favicon.ico | 
## store
محل قرارگیری فایل های استور (Store) اینجا می باشد. در این فولدر دو مدل استفاده از سیستم ویواکس (vueX) که کلاسیک و مدرن می باشد می تواند استفاده کرد. نام هر فایل نام کلی استور را تعیین می کند که در برنامه قابل استفاده می باشد.
از این فایل ها فقط در خود وب سایت و سمت مرورگر استفاده می شود و در پیش پردازش سمت سرور استفاده نمی شوند. مثلا فونت ها و عکس ها و یا موزیک ها در این فولدر می توانند قرار بگیرند و از سمت سایت دانلود شوند.
به صورت پیشفرض استور در ناکس فعال نمی باشد. با ایجاد فایل index.js در این فولدر استور به صورت اتوماتیک فعال می شود.

نام این پوشه قابل تغییر نمی باشد.
## nuxt.confog.js
این فایل شامل تنظیمات دلخواه ناکس می باشد. این فایل را نمی توان تغییر نام داد.

## نام های مستعار 
برای import کردن یک فایل در کل برنامه می توانید از نام های مستعار @ و ~ که معرف روت پروژه هستند استفاده کنید.

| علامت        | دایرکتوری           | 
| ------------- |:-------------:| 
| ~ یا @       | srcDir | 
| ~~ یا @@  | rootDir |

::: tip
در حالت عادی srcDir و rootDir یکی هستند.
:::

```js
import MyComponent from '~/components/MyComponent.vue';
```