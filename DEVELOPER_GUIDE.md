# دليل المطور Cyber Security Guard Pro  
© 2025 Alaa Mahmoud — جمهورية مصر العربية  
📧 alaat9080@gmail.com

---

## 📚 جدول المحتويات

- [مقدمة](#مقدمة)
- [هيكل المشروع](#هيكل-المشروع)
- [إعداد بيئة التطوير](#إعداد-بيئة-التطوير)
- [تهيئة الأدوات](#تهيئة-الأدوات)
- [إعداد Docker (اختياري)](#إعداد-docker-اختياري)
- [معايير البرمجة](#معايير-البرمجة)
- [الاختبارات](#الاختبارات)
- [النشر والتوزيع](#النشر-والتوزيع)
- [المساهمة](#المساهمة)
- [استكشاف الأخطاء](#استكشاف-الأخطاء)
- [خاتمة](#خاتمة)

---

## 🧭 مقدمة

مرحبًا بك في دليل المطور الخاص بـ CyberGuard Pro!  
هذا الدليل موجه للمطورين الذين يرغبون في:

- فهم هيكل المشروع والكود المصدري  
- المساهمة في تطوير الميزات الجديدة  
- تكامل النظام مع أدوات خارجية  
- تطبيق أفضل ممارسات الأمن السيبراني

### المتطلبات الأساسية

- خبرة متوسطة إلى متقدمة في Python  
- فهم أساسيات الأمن السيبراني  
- معرفة بـ SQLAlchemy و REST API  
- أدوات تطوير مثل VS Code أو PyCharm

---

## 🗂️ هيكل المشروع

```text
cyberguard-pro/
├── app/
│   ├── config.py
│   ├── database.py
│   ├── models.py
│   ├── utils.py
│   ├── auth/
│   ├── monitoring/
│   ├── security/
│   ├── ai/
│   ├── reporting/
│   └── api/
├── data/
├── logs/
├── tests/
├── docs/
├── scripts/
├── requirements.txt
├── requirements-dev.txt
├── .env.example
├── run.py
└── README.md


⚙️ إعداد بيئة التطوير
1. استنساخ المستودع
git clone https://github.com/alaat9080-svg/cyber-security-guard-pro.git
cd cyber-security-guard-pro
2. إنشاء بيئة افتراضية
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows
3. تثبيت المتطلبات
pip install -r requirements.txt
pip install -r requirements-dev.txt
4. إعداد pre-commit hooks
pre-commit install
5. تهيئة متغيرات البيئة
cp .env.example .env
# عدل .env حسب إعداداتك


🧰 تهيئة الأدوات
VS Code
تثبيت الإضافات
code --install-extension ms-python.python
code --install-extension ms-python.vscode-pylance
code --install-extension ms-python.debugpy
code --install-extension ms-python.black-formatter
code --install-extension ms-python.isort

إعدادات VS Code
{
  "python.defaultInterpreterPath": "./venv/bin/python",
  "python.linting.enabled": true,
  "python.linting.pylintEnabled": true,
  "python.formatting.provider": "black",
  "python.sortImports.args": ["--profile", "black"],
  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    "source.organizeImports": true
  }
}

PyCharm
افتح المشروع: File > Open > cyberguard-pro

إعداد المترجم: File > Settings > Project: cyberguard-pro > Python Interpreter > Add > Existing Environment اختر: venv/bin/python

إعداد أدوات الجودة: File > Settings > Tools > External Tools أضف: Black, isort, flake8, mypy

🐳 إعداد Docker (اختياري)FROM python:3.9-slim

WORKDIR /app

RUN apt-get update && apt-get install -y \
    gcc \
    g++ \
    && rm -rf /var/lib/apt/lists/*

يمكنك تخصيص Dockerfile حسب بيئة التشغيل الخاصة بك.

🧪 معايير البرمجة
الالتزام بـ PEP8

استخدام Black لتنسيق الكود

استخدام isort لترتيب الاستيرادات

استخدام flake8 و mypy للتحقق من الجودة والأنواع

🧬 الاختبارات
جميع الاختبارات موجودة داخل مجلد tests/

استخدم pytest لتشغيل الاختبارات

اختبارات الوحدة والتكامل مفعّلة

🚀 النشر والتوزيع
يتم تشغيل التطبيق عبر run.py

يمكن نشره باستخدام Docker أو على خادم داخلي

يدعم التوزيع على بيئات Linux و Windows و macOS

🤝 المساهمة
راجع ملف CONTRIBUTING.md

أنشئ فرعًا جديدًا لكل ميزة أو إصلاح

أرسل Pull Request مع وصف واضح واختبارات مرفقة

🛠️ استكشاف الأخطاء
تم توثيق المشاكل الشائعة وحلولها داخل SUPPORT_GUIDE.md، مثل:

تعارض المنافذ

مشاكل في المراقبة أو التنبيهات

بطء الأداء أو مشاكل في قاعدة البيانات

مشاكل في واجهة الويب أو إعدادات البريد

🏁 خاتمة
هذا الدليل يغطي جميع جوانب تطوير CyberGuard Pro، من إعداد البيئة إلى التكامل مع الأدوات الخارجية. إذا كنت بحاجة إلى دعم إضافي، لا تتردد في التواصل مع فريق المشروع.

الأمن السيبراني ليس مجرد كود، بل فلسفة مستمرة. وCyberGuard Pro هو انعكاس لفكر عربي أصيل في بناء أنظمة دفاعية متكاملة.

📧 alaat9080@gmail.com 📍 جمهورية مصر العربية

إنشاء Dockerfile.dev
