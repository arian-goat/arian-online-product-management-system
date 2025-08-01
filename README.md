# arian-online-product-management-system
A full-stack online product management system built with Python Flask, SQLite, HTML, CSS, and JavaScript. Developed by Arian Rahimi
# سیستم مدیریت محصولات آنلاین - Arian's Product Hub

**توسعه‌دهنده:** [آرین رحیمی](https://github.com/arian-goat)

این پروژه یک سیستم مدیریت محصولات آنلاین کامل (Full-Stack) است که با استفاده از تکنولوژی‌های مدرن وب پیاده‌سازی شده است. این سیستم به کاربران اجازه می‌دهد محصولات را اضافه، مشاهده، جستجو، ویرایش و حذف کنند. طراحی آن به گونه‌ای است که هم برای توسعه‌ی محلی با SQLite و هم برای دپلویمنت ابری با PostgreSQL آماده است.

---

## تکنولوژی‌های استفاده شده

### بک‌اند (Backend)
* **پایتون (Python):** زبان برنامه‌نویسی اصلی برای منطق سرور.
* **فلسک (Flask):** یک فریم‌ورک سبک و قدرتمند برای ساخت وب‌سرویس‌ها و API.
* **PostgreSQL:** پایگاه داده رابطه‌ای قدرتمند و پایدار برای محیط‌های دپلوی شده.
* **SQLite:** پایگاه داده سبک و مبتنی بر فایل برای توسعه و تست محلی.
* **Psycopg2:** درایور پایتون برای PostgreSQL.
* **Gunicorn:** یک وب سرور WSGI برای اجرای برنامه‌های پایتون در محیط‌های تولید.
* **Flask-CORS:** برای مدیریت سیاست‌های Cross-Origin Resource Sharing (ارتباط بین فرانت‌اند و بک‌اند در دامنه‌های مختلف).

### فرانت‌اند (Frontend)
* **HTML5:** ساختار و محتوای صفحات وب.
* **CSS3:** استایل‌دهی و طراحی رابط کاربری (شامل طراحی ریسپانسیو).
* **جاوااسکریپت (JavaScript):** برای منطق تعاملی، درخواست‌های API و مدیریت DOM.
* **Fetch API:** برای برقراری ارتباط با API بک‌اند.

---

## قابلیت‌ها

* **افزودن محصول:** امکان اضافه کردن محصولات جدید با نام، توضیحات و قیمت.
* **نمایش محصولات:** نمایش لیست تمام محصولات موجود.
* **جستجوی محصولات:** قابلیت جستجو بر اساس نام یا توضیحات محصول (Case-insensitive).
* **ویرایش محصول:** به‌روزرسانی اطلاعات محصولات موجود از طریق یک مودال کاربرپسند.
* **حذف محصول:** حذف محصولات از سیستم.
* **رابط کاربری ریسپانسیو:** طراحی شده برای نمایش مناسب در دستگاه‌های مختلف (موبایل، تبلت، دسکتاپ).
* **پشتیبانی از دو نوع دیتابیس:** سوئیچ خودکار بین SQLite (محلی) و PostgreSQL (دپلوی شده).

---

## دمو زنده (Live Demo)

شما می‌توانید نسخه دپلوی شده این پروژه را در لینک‌های زیر مشاهده کنید:

* **فرانت‌اند (Frontend - Netlify):** [**YOUR_NETLIFY_URL**](YOUR_NETLIFY_URL)
    * _این لینک پس از دپلوی فرانت‌اند در Netlify قابل دسترسی خواهد بود._

* **بک‌اند (Backend - Heroku/Render/Railway):** [**YOUR_BACKEND_URL**](YOUR_BACKEND_URL)
    * _این لینک پس از دپلوی بک‌اند در پلتفرم ابری (مثل Heroku) قابل دسترسی خواهد بود._

---

## نصب و اجرای پروژه به صورت محلی

برای اجرای این پروژه در سیستم خود، مراحل زیر را دنبال کنید:

1.  **کلون کردن ریپازیتوری:**
    ```bash
    git clone [https://github.com/arian-goat/arian-product-hub-fullstack.git](https://github.com/arian-goat/arian-product-hub-fullstack.git) # نام ریپازیتوری شما ممکن است متفاوت باشد
    cd arian-product-hub-fullstack # به پوشه پروژه بروید
    ```

2.  **ایجاد و فعال‌سازی محیط مجازی پایتون:**
    ```bash
    python -m venv venv
    # برای ویندوز:
    .\venv\Scripts\activate
    # برای مک/لینوکس:
    source venv/bin/activate
    ```

3.  **نصب وابستگی‌های پایتون:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **اجرای سرور بک‌اند (Flask):**
    ```bash
    python app.py
    ```
    سرور بک‌اند شما روی `http://127.0.0.1:5000/` اجرا خواهد شد و از پایگاه داده SQLite استفاده می‌کند.

5.  **اجرای فرانت‌اند:**
    فایل `frontend/index.html` را در مرورگر خود باز کنید.
    **(نکته:** برای ارتباط فرانت‌اند محلی با بک‌اند محلی، مطمئن شوید که خط `const API_BASE_URL = 'http://127.0.0.1:5000';` در `frontend/script.js` فعال باشد و خط مربوط به URL دپلوی شده بک‌اند کامنت شده باشد. اگر مرورگر خطای CORS داد، ممکن است نیاز به نصب یک افزونه مرورگر CORS (مانند "CORS Everywhere" برای Chrome/Firefox) داشته باشید، زیرا مرورگرها به طور پیش‌فرض اجازه درخواست‌های AJAX از یک فایل محلی (`file://`) به یک سرور (`http://`) را نمی‌دهند.)

---

## تماس با توسعه‌دهنده

* **نام:** آرین رحیمی
* **گیت‌هاب:** [arian-goat](https://github.com/arian-goat)
* **ایمیل:** [ایمیل شما (اختیاری)]
* **لینکدین:** [پروفایل لینکدین شما (اختیاری)]

---

**با عشق توسط آرین رحیمی**
