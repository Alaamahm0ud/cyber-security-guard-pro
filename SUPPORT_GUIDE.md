# دليل الدعم الفني واستكشاف الأخطاء  
Cyber Security Guard Pro © 2025 Alaa Mahmoud  
📧 support@cyberguard-pro.com | 📞 +201122595905
📍 جمهورية مصر العربية

---

## 🧭 جدول إنشاء التقارير

```yaml
reporting:
  schedules:
    weekly:
      day: "monday"
      time: "09:00"
      include_trends: true
      include_compliance: true
      distribution:
        - email: management@company.com
        - save_to_database: true
    
    monthly:
      day: 1
      time: "09:00"
      include_strategic_analysis: true
      include_compliance: true
      distribution:
        - email: executives@company.com
        - save_to_database: true

compliance:
  frameworks:
    - gdpr
    - hipaa
    - pci_dss
    - iso27001
  
  assessments:
    frequency: "monthly"
    auto_generate: true
    remediation_plans: true
🛠️ استكشاف الأخطاء الشائعة
1. لا يمكن بدء التطبيق
السبب: تعارض في المنافذ أو مكتبات مفقودة الحل:
netstat -tuln | grep :5000
sudo lsof -ti:5000 | xargs kill -9
pip install -r requirements.txt --force-reinstall

2. المراقبة لا تعمل
السبب: إعدادات غير صحيحة أو مشكلة في الصلاحيات الحل:
python -c "import config; print(config.MONITOR_INTERVALS)"
sudo chown -R $USER:$USER /var/log/cyberguard/
sudo chmod -R 755 /var/log/cyberguard/
python run.py --run-once

3. لا تظهر التنبيهات
السبب: إعدادات البريد الإلكتروني أو مشكلة في الشبكة الحل:
from app.config import Config
print(Config.SMTP_SERVER, Config.SMTP_PORT, Config.EMAIL_ENABLED)
import smtplib
server = smtplib.SMTP('smtp.gmail.com', 587)
server.starttls()
server.login('your_email@gmail.com', 'your_password')
server.quit()
4. أداء النظام بطيء
السبب: بيانات كثيرة أو مشكلة في قاعدة البيانات الحل:
htop
ls -lh /var/lib/cyberguard/cyberguard.db
sqlite3 /var/lib/cyberguard/cyberguard.db "VACUUM;"
tail -n 50 /var/log/cyberguard/cyberguard.log
5. لا يمكن الوصول إلى واجهة الويب
السبب: الخادم لا يعمل أو مشكلة في جدار الحماية الحل:
sudo systemctl status cyberguard-pro
sudo systemctl restart cyberguard-pro
sudo ufw allow 5000/tcp
sudo journalctl -u cyberguard-pro -n 50

📝 إنشاء تقرير خطأ
## تقرير خطأ

### معلومات النظام
- نظام التشغيل: Ubuntu 20.04
- إصدار CyberGuard Pro: 3.0.0
- Python: 3.9.7
- المتصفح: Chrome 90

### وصف المشكلة
[وصف المشكلة التي تواجهها بالتفصيل]

### خطوات إعادة الإنتاج
1. [الخطوة 1]
2. [الخطوة 2]
3. [الخطوة 3]

### النتائج المتوقعة
[ما كنت تتوقع أن يحدث]

### النتائج الفعلية
[ما حدث بالفعل]

### رسائل الخطأ
[أدخل رسائل الخطأ الكاملة هنا]

### لقطات الشاشة
[أرفق لقطات شاشة توضح المشكلة]

### الملفات المرفقة
[أرفق أي ملفات سجلات أو تكوينات ذات صلة]
