# بردیا علیزاده · Farland_game

[English](https://github.com/FarlandGame) | [日本語](https://github.com/FarlandGame/FarlandGame/blob/main/docs/README.ja.md) | [فارسی](https://github.com/FarlandGame/FarlandGame/blob/main/docs/README.fa.md)

من **بردیا علیزاده** هستم؛ ملقب به **کبیر** و شناخته‌شده با نام هنری **Farland_game**. این صفحه محل معرفی پروژه‌های نرم‌افزاری و آثار خلاقانهٔ من است.

## نمونه‌کارها

### [Vexland_Manhunt](https://github.com/FarlandGame/Vexland_Manhunt)

**یک تجربهٔ کامل رانر در برابر هانتر در ماینکرافت، ساختهٔ مشترک [بردیا علیزاده، ملقب به کبیر · Farland_game](https://github.com/FarlandGame) و [علی · Alivexor](https://github.com/Alivexor).**

Vexland_Manhunt آماده‌سازی مسابقه، نقش‌های تیمی، شروع تعقیب‌وگریز، ردیابی، پیشرفت، پاداش‌ها، نتایج و مدیریت را در یک پلاگین سرور Paper گرد هم می‌آورد. رانرها تلاش می‌کنند اندر دراگون را شکست دهند و هانترها سعی می‌کنند آخرین رانر را حذف کنند. پلاگین از چند رانر پشتیبانی می‌کند و تعقیب‌وگریز را در جریان مرگ بازیکنان، بازگشت پس از مرگ، جابه‌جایی بین بُعدها و اتصال مجدد ادامه می‌دهد. مرکز کنترل `/mhgui` به مدیران اجازه می‌دهد مسابقه را از طریق منوها اداره کنند؛ بازیکنان نیز پیام‌ها و کتاب‌های راهنما را به زبان انتخاب‌شده دریافت می‌کنند.

#### دانلود و سازگاری

| نسخهٔ پلاگین | دانلود | محیط هدف |
| --- | --- | --- |
| **1.9.11** — نسخهٔ فعلیِ دریافت‌شده | [VexLandManhunt-1.9.11-.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.9.11/VexLandManhunt-1.9.11-.jar) | Paper **1.21.11**، Java **21** |
| **1.6.4** — نسخهٔ قدیمی‌تر | [VexLandManhunt-1.6.4.jar](https://github.com/FarlandGame/Vexland_Manhunt/releases/download/v1.6.4/VexLandManhunt-1.6.4.jar) | Paper **1.21.11**، Java **21** |

**1.6.4 و 1.9.11 شمارهٔ نسخه‌های پلاگین هستند.** هر دو فایل دریافت‌شده، Minecraft API `1.21.11` و کلاس‌های Java 21 را مشخص کرده‌اند. این فایل‌ها پلاگین سرور برای Minecraft Java Edition هستند. [نیازمندی Java در نسخه‌های مختلف Paper](https://docs.papermc.io/paper/getting-started/) نیز Java 21 را برای Paper 1.21.11 اعلام می‌کند. در مشخصات همراه این دو نسخه، وابستگی به پلاگین دیگری ثبت نشده است.

این فایل‌ها **نسخه‌های اصلیِ سرور شخصی با دسترسی مدیریتیِ بالاترِ مخصوص سازندگان** هستند و دقیقاً به همان شکل دریافت‌شده نگهداری شده‌اند. راهنمای زیر کنترل‌های عمومی منهانت را توضیح می‌دهد.

#### تجربهٔ منهانت

- **تیم‌های رانر و هانتر:** بازیکنان آنلاین را در یکی از دو تیم قرار دهید. مسابقه به حداقل یک رانر و یک هانتر یا بازیکن آنلاینِ بدون نقش نیاز دارد. با مرگ یک هم‌تیمی، رانرهای زنده مسابقه را ادامه می‌دهند؛ رانرِ کشته‌شده به هانتر تبدیل می‌شود، مگر اینکه همان مرگ مسابقه را تمام کند.
- **شروع سینمایی مسابقه:** موجودی بازیکنان و حالت‌های بازی آماده می‌شوند، تیم‌ها معرفی می‌شوند و گردونه، فرصت فرار اولیهٔ رانرها را تعیین می‌کند. هانترها در طول شمارش معکوس متوقف می‌مانند و عنوان‌های روی صفحه و صداها وضعیت را اعلام می‌کنند. فرصت فرار تصادفی است؛ مدیران می‌توانند هانترها را زودتر آزاد کنند.
- **قطب‌نمای ردیاب با انتخاب هدف:** هانترها یک قطب‌نمای ویژه دریافت می‌کنند. با راست‌کلیک، رانری را از منوی هدف انتخاب کنید و در جریان تعقیب هدف را تغییر دهید. در بُعدهای متفاوت، ردیاب مسیر پورتال مربوط را دنبال می‌کند تا ردیابی مستقیم دوباره ممکن شود. هانترها پس از بازگشت از مرگ، ردیاب خود را دوباره دریافت می‌کنند.
- **نمایش پیشرفت:** باس‌بارها و اطلاعات مسابقه، تجهیزات رانر و پیشرفت او را در منابع ندر، بلیز راد، اندر پرل، چشم اندر، استرانگهولد و اند دنبال می‌کنند. نسخهٔ جدیدتر مرحله‌های دقیق‌تر و نمایش پیشرفتی متناسب با سلامت دراگون اضافه می‌کند.
- **پاداش برای کشتن هانتر توسط رانر:** وقتی رانر در یک مسابقهٔ فعال هانتر را می‌کشد، یک مجموعهٔ وزن‌دار از 50 پاداش، با در نظر گرفتن پیشرفت بازی، استفاده می‌شود. انتخاب‌های تصادفی همراه با انیمیشن، پاداش‌های دوبل و تریپل، اعلان زنجیرهٔ کشتن و جشن آیتم‌های کمیاب در این سیستم وجود دارند.
- **پیروزی و نتایج:** مرگ آخرین رانر، هانترها را برنده می‌کند؛ شکست اندر دراگون، پیروزی رانرها را به همراه دارد. عنوان پایان مسابقه، جشن، آمار کشتن و مرگ، و پاک‌سازی آیتم‌های موقت نیز وجود دارند. نسخهٔ جدیدتر آمار MVP، آسیب و مسافت را هم گزارش می‌کند.
- **ارتباط تیمی و ابزارها:** پیام خصوصی به هم‌تیمی‌ها با `/teammsg`، موجودی دورریختنیِ 54 خانه‌ای با `/trash` و دید در شب شخصی با `/nv`.
- **مدیریت از طریق منوها:** نقش‌ها، شروع و ریست، آزادی زودهنگام هانترها، آسیب به هم‌تیمی، قفل سرور، انتقال همه، پرکردن سلامت و غذا، زبان، تنظیمات حفاظتی، وضعیت و کتاب‌های راهنما در مرکز کنترل در دسترس هستند. توقف بازیکنان و ریست کامل به آماده‌سازی مسابقهٔ بعدی کمک می‌کنند.
- **راهنماهای چندزبانه:** کتاب‌های رانر، هانتر و مدیر، هدف‌ها، استفاده از ردیاب، مرگ، آماده‌سازی و دستورها را توضیح می‌دهند. در نسخهٔ 1.9.11، بازیکنان با `/mhhelp` راهنمای متناسب با نقش خود دریافت می‌کنند.
- **اتصال به Anti-Xray در Paper:** کنترل‌های منو، حفاظت Paper در سطح دنیا را تنظیم می‌کنند؛ برای اعمال تغییرات باید سرور دوباره راه‌اندازی شود.

#### چه چیزهایی در 1.9.11 تازه هستند؟

این تغییرات با مقایسهٔ دو نسخهٔ دریافت‌شده، از جمله مشخصات، منابع پیام‌ها و کلاس‌های کامپایل‌شدهٔ آن‌ها شناسایی شده‌اند.

| قابلیت یا تغییر | رفتار در 1.9.11 |
| --- | --- |
| **Smart Hunter Kit V3** | کیت‌های سازگارشوندهٔ بازگشت پس از مرگ، تجهیزات رانر، تیم‌ها و شرایط مسابقه را در نظر می‌گیرند. هدف سیستم این است که تجهیزات هانتر از میانگین تجهیزات رانرها ضعیف‌تر بمانند. می‌توان آن را با `/mhkit` یا رابط گرافیکی روشن و خاموش کرد. |
| **اسپاون خودکار اورورلد** | اسپاون دنیا در بازهٔ انتخاب‌شده به نزدیکی یک رانر واجد شرایط در اورورلد منتقل می‌شود: خاموش، 5، 10، 15، 20 یا 30 دقیقه. سیستم یک نقطهٔ امن روی سطح انتخاب می‌کند و وضعیت‌های نامناسب را نادیده می‌گیرد. |
| **مکث و ادامه** | `/mhpause` گیم‌پلی، زمان‌سنج‌های مرتبط با مسابقه، ردیابی و جابه‌جایی اسپاون را متوقف می‌کند؛ `/mhresume` آن‌ها را ادامه می‌دهد. زمان مکث از زمان فعال مسابقه کنار گذاشته می‌شود. |
| **بازیابی پس از راه‌اندازی مجدد یا کرش** | یک لایهٔ بازیابی با استفاده از ذخیره‌های اصلی و پشتیبان، ذخیره‌های دوره‌ای و ذخیره هنگام خاموش‌شدن، وضعیت مسابقه، نقش‌ها، هدف‌های ردیاب، پیشرفت، زمان‌سنج‌های پاداش و مرگ و وضعیت اتصال مجدد را برمی‌گرداند. |
| **تنظیمات اتصال مجدد رانر** | مهلت قابل تنظیمِ اتصال مجدد جایگزین مهلت ثابت 60 دقیقه‌ایِ قبلی می‌شود. مقدار پیش‌فرض نصب تازه 15 دقیقه است و بازگشت بازیکن 10 ثانیه حفاظت دارد. زمان خاموش‌بودن سرور حساب نمی‌شود؛ پایان مهلت می‌تواند رانر را به هانتر تبدیل کند یا مسابقه را تمام کند. |
| **مدیریت گسترده‌تر** | تغییر نقش‌ها حین مسابقه با حفاظت از آخرین رانر، عملیات روی بازیکن انتخاب‌شده، انتقال و توقف تیم، همگام‌سازی مجدد وضعیت اجرایی و میان‌برها، مدیریت مسابقه را بهتر می‌کنند. |
| **ریست تنظیمات با تأیید** | دو کلیک در فاصلهٔ هشت ثانیه، Smart Kit را روشن، اسپاون خودکار را روی هر 15 دقیقه و مهلت اتصال مجدد را روی 15 دقیقه تنظیم می‌کنند. این با نصب تازه تفاوت دارد؛ اسپاون خودکار در نصب تازه خاموش است. |
| **VexAC 3.0** | بررسی حرکت، مبارزه، AutoClick، سرعت و ضربهٔ عقب‌راننده، و ساخت‌وساز دنیا؛ کنترل گروه‌ها و کل سیستم، ثبت شواهد، هشدار به مدیران و معافیت‌های مربوط به محیط و تأخیر سرور. |
| **Ultra Deep Debug v4** | `/mhdebug` بررسی‌های تشخیصیِ ماشین حالت، رابط گرافیکی، کیت مصنوعی و فشار، جای‌نگهدارهای زبان، ذخیره و بازیابی و یکپارچگی را فراهم می‌کند. |
| **نمایش‌های گسترده‌تر** | جزئیات بیشتر پیشرفت، نمایش سلامت دراگون، نتایج MVP، آسیب و مسافت، و اطلاعات پینگ در TAB. |
| **تغییر دستورها** | `/mhkit`، `/mhspawn`، `/mhpause`، `/mhresume` و `/mhdebug` اضافه می‌شوند؛ `/mhnone` حذف می‌شود؛ `/mhhelp` راهنمای بازیکن و مدیر را متناسب ارائه می‌کند و نام‌های جایگزین برای `/trash` اضافه می‌شوند. |
| **پیام‌های چندزبانهٔ بیشتر** | منابع ترجمه از 446 کلید پیام برای هر زبان به 683 کلید گسترش می‌یابند. |

بررسی‌های موجود در VexAC شامل Fly، Speed، Timer، Phase، Step، NoSlow، GroundSpoof، Reach، KillAura، AimAssist، wall-hit، BadPackets، الگوهای زمانی AutoClick، دست‌کاری ضربهٔ عقب‌راننده، Scaffold، Tower، FastPlace، Nuker و دسترسی به بلوک از فاصلهٔ غیرمجاز هستند. رابط آن برچسب «فقط نظارت» دارد، اما کد کامپایل‌شده مسیرهای اخراج بازیکن را هم در خود دارد؛ پیش از اعتماد به آن برچسب، رفتار واقعیِ برخورد با بازیکنان را روی یک سرور آزمایشی بررسی کنید. نسخهٔ قدیمی‌تر به‌جای این سیستم، کنترل‌های قدیمی Anti AutoClick و Anti Fly را دارد.

#### شروع استفاده با `/mhgui`

1. یکی از فایل‌های JAR را روی سرور Paper 1.21.11 با Java 21 نصب کن و سرور را کامل ری‌استارت کن.
2. با حساب OP مورداعتماد وارد شو و **`/mhgui`** را اجرا کن.
3. در **Player Roles** روی سر بازیکنان کلیک کن و حداقل یک Runner و یک Hunter تعیین کن.
4. **Friendly Fire**، **Language**، **Smart Hunter Kit** و **Auto World Spawn** را بررسی کن و **Server Freeze** را خاموش کن.
5. **Start Match** را بزن. شکارچی‌ها پس از آزادشدن با راست‌کلیک روی قطب‌نما Runner را انتخاب می‌کنند.
6. در 1.9.11 از Pause/Resume استفاده کن؛ برای دور تازه Reset Match را بزن.

**[راهنمای کامل منو و تمام فرمان‌ها](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.fa.md)**

#### یک کری‌خوانی دوستانه با دریم

کمی شوخی و کری‌خوانیِ ماینکرافتی از بردیا 😄

> هعی، پلاگین منهانت من و علی صد برابر بهتر از دریم شده، ولی دریم ترسیده و پلاگین ما رو بازی نمی‌کنه!

**زبان‌های توضیحات (18):**

[English](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/README.md) · [日本語](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.ja.md) · [فارسی](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.fa.md) · [Deutsch](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.de.md) · [Français](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.fr.md) · [Español](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.es.md) · [Português (Brasil)](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.pt-BR.md) · [Italiano](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.it.md) · [Nederlands](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.nl.md) · [Polski](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.pl.md) · [Українська](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.uk.md) · [Türkçe](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.tr.md) · [Русский](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.ru.md) · [简体中文](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.zh-CN.md) · [繁體中文](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.zh-TW.md) · [한국어](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.ko.md) · [हिन्दी](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.hi.md) · [Bahasa Indonesia](https://github.com/FarlandGame/Vexland_Manhunt/blob/main/docs/README.id.md)

### [Farland_autcliker](https://github.com/FarlandGame/Farland_autcliker)

<!-- APP_DOCUMENTATION -->
**زبان‌های توضیحات (18):**

[English](https://github.com/FarlandGame/Farland_autcliker/blob/main/README.md) · [日本語](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.ja.md) · [فارسی](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.fa.md) · [Deutsch](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.de.md) · [Français](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.fr.md) · [Español](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.es.md) · [Português (Brasil)](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.pt-BR.md) · [Italiano](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.it.md) · [Nederlands](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.nl.md) · [Polski](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.pl.md) · [Українська](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.uk.md) · [Türkçe](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.tr.md) · [Русский](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.ru.md) · [简体中文](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.zh-CN.md) · [繁體中文](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.zh-TW.md) · [한국어](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.ko.md) · [हिन्दी](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.hi.md) · [Bahasa Indonesia](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.id.md)

**[دانلود نسخهٔ ویندوز](https://github.com/FarlandGame/Farland_autcliker/releases/latest/download/Farland_autcliker.zip)** · [مشاهدهٔ کد منبع](https://github.com/FarlandGame/Farland_autcliker) · [راهنمای فارسی](https://github.com/FarlandGame/Farland_autcliker/blob/main/docs/README.fa.md)

Farland_autcliker یک برنامهٔ ویندوزی ساختهٔ **بردیا علیزاده، ملقب به کبیر، با نام هنری Farland_game** است. ویژگی اصلی آن به شیوهٔ آغاز کلیک‌های خودکار برمی‌گردد: **هر کلیک واقعی موس، یک نوبت مستقل از کلیک‌های اضافه را در طول یک ثانیه آغاز می‌کند.** این طراحی برای کسی مناسب است که می‌خواهد زمان شروع کلیک‌های اضافه را با حرکت و کلیک خودش تعیین کند و تنظیمات کلیک چپ و راست را جداگانه در اختیار داشته باشد. رابط فارسی، کنترل‌های قابل تغییر، ذخیرهٔ تنظیمات و نسخهٔ اجرایی آمادهٔ ویندوز، این رفتار را در یک برنامه جمع می‌کنند.

#### کلیک خودت چگونه به کلیک‌های اضافه تبدیل می‌شود؟

ابتدا اتوکلیکر را روشن کن و بعد دکمهٔ چپ یا راست موس را فشار بده. کلیک واقعی به‌صورت عادی ثبت می‌شود و برنامه، کلیک‌های اضافه با همان دکمه را برای یک ثانیهٔ بعد برنامه‌ریزی می‌کند. برای مثال، اگر سمت چپ روی **۲۰ CPS** باشد، یک کلیک واقعی چپ، **۲۰ کلیک اضافهٔ چپ** ایجاد می‌کند. با احتساب کلیک واقعی، مجموعاً ۲۱ کلیک درخواست می‌شود؛ ثبت آن‌ها به نحوهٔ پردازش ورودی برنامهٔ مقصد هم بستگی دارد.

اگر پیش از پایان نوبت اول دوباره کلیک کنی، نوبت دیگری شروع می‌شود. دو کلیک واقعی چپ، مجموعاً ۴۰ کلیک اضافه را در دو بازهٔ یک‌ثانیه‌ای که ممکن است هم‌پوشانی داشته باشند، برنامه‌ریزی می‌کنند. بنابراین عدد CPS مربوط به **هر نوبت مستقل** است و سقف مجموع نوبت‌های هم‌زمان نیست. وقتی کلیک واقعی تازه‌ای انجام ندهی، نوبت تازه‌ای ساخته نمی‌شود؛ نوبت‌های قبلی تا پایان یا خاموش‌کردن اتوکلیکر ادامه پیدا می‌کنند.

#### تفاوت شیوهٔ کار با حالت تکرار پیوسته

در [حالت تکرار تا زمان توقف](https://www.opautoclicker.com/)، با شروع برنامه یک زنجیرهٔ تکراری از کلیک‌ها اجرا می‌شود. ویژگی متمایز Farland_autcliker، **شروع نوبت‌های اضافه با هر کلیک واقعی** و تنظیم مستقل دو سمت موس است.

| رفتار | حالت تکرار تا توقف | Farland_autcliker |
| --- | --- | --- |
| آغاز کلیک اضافه | شروع زنجیرهٔ تکرار | روشن‌کردن و سپس کلیک واقعی |
| کلیک واقعی تازه | برای ادامهٔ تکرار لازم نیست | نوبت مستقل تازه‌ای می‌سازد |
| پایان یک نوبت | توقف زنجیرهٔ تکرار | پایان برنامهٔ یک‌ثانیه‌ای همان نوبت |

این جدول دو شیوهٔ کار را مقایسه می‌کند؛ اتوکلیکرهای دیگر ممکن است حالت‌های بیشتری هم داشته باشند. ویژگی‌های این برنامه بر اساس رفتار قابل مشاهده در کد معرفی شده‌اند.

#### اختیار جداگانه برای چپ و راست

سرعت هر سمت از **۱ تا ۱۰٬۰۰۰ CPS** قابل تنظیم است و می‌توان هر سمت را جداگانه روشن یا خاموش کرد. مثلاً چپ را روی ۲۰ و راست را روی ۸ بگذار: کلیک چپ، نوبت کلیک‌های چپ را آغاز می‌کند و کلیک راست، نوبت مستقل کلیک‌های راست را. وقتی یک سمت غیرفعال باشد، کلیک واقعی آن به شکل عادی عمل می‌کند و کلیک اضافهٔ تازه‌ای نمی‌سازد.

#### کنترل‌هایی متناسب با شیوهٔ استفادهٔ تو

روشن و خاموش کردن با دکمهٔ اصلی برنامه یا میانبر سراسری انجام می‌شود. می‌توانی کلیک وسط، هر یک از دکمه‌های کناری موس، F6 تا F9، Home، End یا Insert را انتخاب کنی. **F12** برای توقف اضطراری و خروج است. چهار تم تیره، روشن، بنفش و آبی هم ظاهر برنامه را قابل انتخاب می‌کنند. سرعت‌ها، وضعیت فعال‌بودن دو سمت، میانبر و تم برای اجرای بعدی ذخیره می‌شوند. اگر مقدار نامعتبری برای سرعت وارد شود، برنامه به آخرین مقدار معتبر برمی‌گردد.

#### مدیریت کلیک‌های اضافه

موتور برنامه ورودی واقعی را از کلیک‌های مصنوعی ویندوز تشخیص می‌دهد؛ به همین دلیل کلیک‌های تولیدشدهٔ خودش، نوبت‌های تازه و چرخهٔ تکراری ایجاد نمی‌کنند. زمان‌بند، نوبت‌های هم‌زمان را مدیریت می‌کند و در سرعت بالا کلیک‌ها را در دسته‌های کوچک می‌فرستد. **۱۰٬۰۰۰ CPS سقف قابل تنظیم است و تضمین سرعت اندازه‌گیری‌شده نیست.** سرعت واقعی به سیستم، پردازش ورودی ویندوز و برنامهٔ مقصد بستگی دارد.

#### دانلود و بررسی پروژه

فایل ZIP عمومی شامل نسخهٔ اجرایی، کد منبع، تصویر برنامه و راهنمای انگلیسی، ژاپنی و فارسی است. پس از استخراج، `Farland-Auto-Clicker/dist/Farland Auto Clicker.exe` را باز کن؛ نسخهٔ اجرایی به نصب جداگانهٔ Python نیاز ندارد. کد برای ویندوز ۱۰ یا ۱۱ و Python 3.10 یا جدیدتر نوشته شده و از Tkinter و Windows API استفاده می‌کند. شش آزمون موجود پروژه، زمان‌بندی، فعالیت هم‌زمان دو سمت، لغو کلیک‌ها، میانبرها و فیلتر ورودی مصنوعی را با کلیک‌های شبیه‌سازی‌شده بررسی می‌کنند.

**فناوری‌ها:** Python · Tkinter · Windows API · PyInstaller

## لینک‌های من

### کانال‌ها و شبکه‌های اجتماعی

| پلتفرم | کانال‌ها / صفحه‌ها |
| --- | --- |
| GitHub | [FarlandGame](https://github.com/FarlandGame) |
| YouTube | [Farland_game](https://www.youtube.com/@Farland_game) · [Farland_animation](https://www.youtube.com/@Farland_animation) |
| کانال‌های روبیکا | [farland_gam](https://rubika.ir/farland_gam) · [Farland_animatio](https://rubika.ir/Farland_animatio) |
| صفحه‌های روبیکا | [farland_game](https://rubika.ir/farland_game) · [Farland_animations](https://rubika.ir/Farland_animations) |
| Instagram | [farland_game](https://www.instagram.com/farland_game/) |
| کانال‌های تلگرام | [Farland_gam](https://t.me/Farland_gam) · [Farland_animatio](https://t.me/Farland_animatio) |
| Twitch | [farlandgame](https://twitch.tv/farlandgame) |
| Kick | [farlandgame](https://kick.com/farlandgame) |
| Aparat | [Farland_Game](https://aparat.com/Farland_Game) |
| SoundCloud | [Bardiya Kabir](https://soundcloud.com/bardiya-kabir-798008614) |

### ربات موسیقی تلگرام

[ربات Farland Music Bot](https://t.me/Farland_Music_bot) — لینک ویدیوی آهنگ موردعلاقه‌ات را به ربات تلگرامی ما بفرست تا آهنگ را پیدا کنی.

### جامعه و خانواده

- **THE APEX:** [یوتیوب](https://www.youtube.com/@THE_APEX_MC) · [تلگرام](https://t.me/+-3uY7eIZArVjZDE0)
- **منهانت:** [گروه تلگرام](https://t.me/+DAq20XrkPyZhNjVk)
- **کانال برادرم:** [ArmiyaFabix در یوتیوب](https://www.youtube.com/@ArmiyaFabix)

### حمایت از کارهای من

[حمایت مالی از طریق ریمیت](https://reymit.ir/farland_game) ❤️
