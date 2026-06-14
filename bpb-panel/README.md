# 🛡️ راهنمای دیپلوی BPB Worker Panel

## 📖 BPB Worker Panel چیه؟

یه پنل رایگان و اوپن‌سورس برای ساخت کانفیگ‌های VPN:
- 🆓 **VLESS, Trojan, Warp** configs
- ☁️ روی **Cloudflare Workers / Pages** دیپلوی می‌شه
- 🛡️ حتی وقتی **Cloudflare یا Warp بلاک** باشن کار می‌کنه
- 🔒 DNS خصوصی + Chain Proxy
- 🚫 بلاک تبلیغات + bypass regional

🔗 **ریپو رسمی:** [github.com/bia-pain-bache/BPB-Worker-Panel](https://github.com/bia-pain-bache/BPB-Worker-Panel)

---

## 🚀 راهنمای قدم‌به‌قدم دیپلوی

### مرحله ۱: ساخت اکانت Cloudflare (رایگان)

1. برو به: [dash.cloudflare.com/sign-up](https://dash.cloudflare.com/sign-up)
2. **Sign up** با ایمیل
3. ایمیلت رو تایید کن
4. ✅ اکانت آماده‌ست!

> 💰 **نکته:** پلن رایگان Cloudflare برای Worker کافیه (۱۰۰,۰۰۰ request/روز)

---

### مرحله ۲: فعال‌سازی Workers

1. تو داشبورد Cloudflare، برو به: **Workers & Pages**
2. روی **Create application** کلیک کن
3. **Create Worker** رو انتخاب کن
4. یه اسم بده (مثلاً `my-bpb-panel`)
5. روی **Deploy** بزن
6. ✅ Worker ساخته شد!

---

### مرحله ۳: دیپلوی BPB Panel

#### روش A — با لینک مستقیم (ساده‌ترین): 🌟

1. برو به این لینک:
   ```
   https://deploy.workers.cloudflare.com/?url=https://github.com/bia-pain-bache/BPB-Worker-Panel
   ```
2. با اکانت Cloudflare وارد شو
3. **Authorize** رو بزن
4. **Fork and Deploy** کلیک کن
5. ✅ BPB Panel دیپلوی شد!

#### روش B — با Wrangler (دستی):

```bash
# نصب wrangler
npm install -g wrangler

# لاگین
wrangler login

# کلون کردن ریپو
git clone https://github.com/bia-pain-bache/BPB-Worker-Panel.git
cd BPB-Worker-Panel

# دیپلوی
wrangler deploy
```

---

### مرحله ۴: تنظیمات پنل

1. به آدرس Worker خودت برو:
   ```
   https://my-bpb-panel.YOUR-SUBDOMAIN.workers.dev
   ```
2. وارد **Settings** شو
3. تنظیمات رو پر کن:
   - 🔐 **Password**: رمز عبور قوی بذار
   - 🌐 **Clean IPs**: IPهای تمیز برای Warp
   - 🔗 **Subscription URL**: لینک subscription خودت
   - 🛡️ **Chain Proxy**: اختیاری
   - 🚫 **Block Ads**: فعال کن

4. **Save** کن

---

### مرحله ۵: استفاده از کانفیگ‌ها

1. تو پنل BPB، از منو **Configs** رو بزن
2. یه کانفیگ انتخاب کن (VLESS / Trojan / Warp)
3. **Generate** بزن
4. 📋 **Copy** کن یا 📷 **QR** بگیر
5. تو اپ VPN (v2rayNG, Hiddify, ...) وارد کن

---

## 📱 اپ‌های پیشنهادی

| اپ | سیستم | لینک |
|----|-------|------|
| 📱 v2rayNG | Android | [GitHub](https://github.com/2dust/v2rayNG/releases) |
| 🚀 Hiddify | Multi | [hiddify.com](https://hiddify.com/) |
| 🍎 V2Box | iOS | [App Store](https://apps.apple.com/app/v2box/id6446448075) |
| 💻 v2rayN | Windows | [GitHub](https://github.com/2dust/v2rayN/releases) |
| 🐱 Nekoray | Linux/Mac | [GitHub](https://github.com/MatsuriDayo/nekoray/releases) |

---

## ⚙️ ویژگی‌های BPB Panel

### 🔐 Fragment + TLS:
- تنظیم SNI, alpn, fingerprint
- انتخاب protocol

### 🌐 Multi Fragment:
- تقسیم ترافیک به چند fragment
- رد شدن از فیلترینگ

### 🔗 Chain Proxy:
- زنجیره کردن چند proxy
- امنیت بیشتر

### 🚫 Ad-Block:
- بلاک تبلیغات تو همه اپ‌ها
- قابل تنظیم

### 📊 Logging:
- لاگ مصرف ترافیک
- مانیتورینگ real-time

---

## 🛠️ عیب‌یابی

### ❌ Worker دیپلوی نمی‌شه
- مطمئن شو subdomain درست وارد شده
- مطمئن شو npm/wrangler به‌روزه

### ❌ کانفیگ‌ها کار نمی‌کنن
- IPهای تمیز رو عوض کن
- Fragment رو فعال کن
- SNI رو به `speed.cloudflare.com` تغییر بده

### ❌ پنل باز نمی‌شه
- Cloudflare اکانتت رو چک کن
- Worker رو Redeploy کن

---

## 📚 منابع بیشتر

- 🔗 [ریپو رسمی BPB](https://github.com/bia-pain-bache/BPB-Worker-Panel)
- 📖 [ویکی BPB](https://github.com/bia-pain-bache/BPB-Worker-Panel/wiki)
- 💬 [تلگرام گروه پشتیبانی](https://t.me/BPB_Group)

---

ساخته شده با ❤️ توسط **Warden VPN**
