# Work Time Tracker Android v9

نسخه اندروید شخصی با ثبت فعالیت زنده، اسکرین‌شات اختیاری، گزارش PDF و Excel، صفحه‌بندی لاگ‌ها، بازیابی رمز و تنظیم بیکاری/توقف.

## تغییرات v9

- اضافه شدن گزینه **فراموشی رمز** در صفحه ورود.
- الگوریتم بازیابی رمز: کد ۴ رقمی ساعت فعلی با فرمت ۲۴ ساعته است؛ مثال 09:15 => 0915 و 19:03 => 1903.
- بعد از ورود کد بازیابی، کاربر می‌تواند رمز جدید انتخاب کند.
- صفحه فعالیت‌ها صفحه‌بندی شد و دیگر همه لاگ‌ها یک‌باره لود نمی‌شوند.
- تعداد آیتم‌های هر صفحه قابل انتخاب است: 10، 15، 20 یا 50.
- پیش‌نمایش اسکرین‌شات داخل کارت فعالیت حذف شده و فقط دکمه **نمایش اسکرین‌شات** وجود دارد.
- خروجی **Excel** اضافه شد. فایل با فرمت XML Spreadsheet و پسوند `.xls` ذخیره می‌شود و در Excel باز می‌شود.
- خروجی PDF و Excel هر دو با فایل‌پیکر اندروید ذخیره می‌شوند تا کاربر نام فایل و مسیر ذخیره را انتخاب کند.
- تنظیمات بیکاری/توقف، تغییر رمز، پاکسازی اسکرین‌شات‌ها و دسترسی‌ها حفظ شده‌اند.

## ساخت APK در GitHub Actions

فایل‌های پروژه را مستقیم در ریشه repo قرار بده؛ یعنی `app`، `.github`، `build.gradle` و `settings.gradle` مستقیم دیده شوند. سپس workflow موجود را از تب Actions اجرا کن.

## دسترسی‌ها

- Usage Access برای ثبت برنامه‌های فعال لازم است.
- Screenshot Accessibility برای ثبت اسکرین‌شات اختیاری لازم است.
- روی Android 13+ ممکن است لازم باشد در App info گزینه Allow restricted settings را فعال کنی.


## v10 bug fixes

- Idle/away timeout no longer stops all logging just because the value is greater than 0.
- Idle time is calculated from real gaps between activity logs and screen/activity gaps, not by blindly closing the active app after the timeout.
- Automatic screenshots are delayed for 3 seconds after entering a new app so the captured screen is more stable.
- Activity cards show friendly/common app names such as Eitaa, Telegram, Chrome, YouTube, etc. The original package name is still shown in the activity details dialog.
- Timeline rendering was fixed to draw all activity segments instead of stopping after a small number of bars. It now uses more lanes and redraws with live data.
