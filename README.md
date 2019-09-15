# jb-dateinput-react

mobx base jalali date input 
most of the time user of the back office and panels always complain about mouse base date input component becuase most of the time they want choose birthday and other old date and they work with keyboard so this keyboard base component add validation and date convertor by defualt and you can specify mask for different standard and it work without any problem.

اغلب اوقات کارمندان شرکت ها و یا سازمان هایی که به طور مرتب با فرم های بزرگ و پیچیده سر کار هستند و با بک آفیس سیستم به طور مرتب کار دارند، از کامپوننت های ورود تاریخ مبتنی بر موس شکایت دارند چرا که برای انتخاب مواردی مثل تاریخ تولد و... باید تعداد زیادی کلیک کرده و وقت بسیاری از آنها میگیرد در حالیکه تایپ تاریخ به صورت ساده برای آنها بسیار راحت تر است . این کامپوننت با قابلیت هایی مثل خروجی شمسی و میلادی با هم و امکان تغییر اینپوت ماسک و یا تغییر مقادیر با کلید های بالا و پایین کیبورد جهت راحتی هر چه بیشتر این افراد طراحی شده است

## installation

run `npm install jb-dateinput-react` to install package with npm

## usage

import component in your page `import JBDateInput from 'jb-dateinput-react'`
you can import special edition for different envirement like es6 or requirejs or systemjs like:
`import JBDateInput from 'jb-dateinput-react/dist/JBDateInput.cjs.min'` for requirejs version
`import JBDateInput from 'jb-dateinput-react/dist/JBDateInput.min'` for standard es6
`import JBDateInput from 'jb-dateinput-react/dist/JBDateInput.systemjs.min'` for systemjs

use in react render like every other component
`<JBDateInput className="your-custome-class" value={this.model.fromDate} config={this.model.fromDateConfig} onChange={(e)=>{this.setInputValue(e,'fromDate');}}></JBDateInput>`
JBDateInput is design so minimal and its not contain any sort of custom style so you can shape it however you want base on your application style.
the `value` property is the string value you want to bind to Component for example `1998-01-04T00:00:00.000` and it is one way binded like every other react standard form element.
the  `config` property is object and must be defined so date input know your date mask standard and defined like this:

`fromDateConfig:{
    inputMask:"yyyy-MM-ddTHH:mm:ss.SSS",
 },`
 the onChange event has a event.detail contain jalali date and garegorian date and standard value base on your config input mask. and you can get value in `event.target.value` that contain user inputed value in garegory format.
 