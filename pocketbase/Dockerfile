# ✅ Dockerfile لتشغيل PocketBase على Railway أو أي سيرفر

FROM alpine:latest

# تثبيت الأدوات المطلوبة
RUN apk add --no-cache ca-certificates

# إنشاء مجلد التطبيق
WORKDIR /app

# إضافة الباينري الخاص بـ PocketBase (يجب نسخه يدويًا بجوار هذا الملف)
COPY pocketbase /app/pocketbase

# إعطاء صلاحية تشغيل
RUN chmod +x /app/pocketbase

# تعيين البورت الافتراضي لـ PocketBase
EXPOSE 8090

# أمر التشغيل
CMD ["./pocketbase", "serve", "--http", "0.0.0.0:8090"]
