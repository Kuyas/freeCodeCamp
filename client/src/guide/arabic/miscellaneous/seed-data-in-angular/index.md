---
title: Seed Data in Angular
localeTitle: بيانات البذور في الزاوي
---
تمثل _الأشياء_ التي تظهر في العرض الرئيسي لتطبيقك جزءًا من بعض بيانات البذور التي تتم إضافتها إلى قاعدة البيانات (بما في ذلك الاختبار ومستخدمي المشرف) في كل مرة تقوم فيها بإعادة تشغيل تطبيقك (عن طريق تشغيل `grunt serve` في سطر الأوامر). يتم تعريف هذه البيانات في **/server/config/seed.js** .

يمكنك إضافة أو إزالة أو تغيير البيانات في هذا الملف ، وسيتم كتابتها إلى قاعدة البيانات الخاصة بك ، مع استبدال أي نسخ مكررة في المرة التالية التي تقوم فيها بتشغيل `grunt serve` . إذا تم الكتابة فوق كائن معرف في **seed.js** ، فستقوم قاعدة البيانات بتعيين كائن جديد _._ الملكية id\_ إليها (ونحن سوف _تغطي._ id\_ العقارات في القسم التالي)، والتي قد تعطيك بعض القضايا في وقت لاحق في الاختبار. لتجنب ذلك ، يمكنك إيقاف عملية `seedDB: false` عن طريق تعيين `seedDB: false` في **/server/config/environment/development.js** .