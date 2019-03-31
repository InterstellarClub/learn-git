---
id: clean
title: clean
---

## الإسم
git-clean : حذف الملفات التي لا يمكن تقفي اثرها في الشجرة العمل

## مُلخّص

<!--DOCUSAURUS_CODE_TABS-->
<!--الأمر-->
```bash
git clean [-d] [-f] [-i] [-n] [-q] [-e <pattern>] [-x | -X] [--] <path>…​
```
<!--END_DOCUSAURUS_CODE_TABS-->

## التفاصيل

 تنظيف شجرة العمل عن طريق إزالة الملفات التي لا تخضع للتحكم في الإصدار بشكل متكرر ، بدءًا من الدليل الحالي  .
في العادة , تتم حذف الملفات الغير معروفة لدى " الجيت " فقط , لكن اذا تم تحديد الخيار
<!--DOCUSAURUS_CODE_TABS-->
<!--الأمر-->
```bash
-x
```
<!--END_DOCUSAURUS_CODE_TABS-->
تتم إزالة الملفات التي تم تجاهلها أيضًا. يمكن أن يكون هذا  مفيدًا لإزالة جميع منتجات الإنشاء على سبيل المثال

اذا تم تقديم اي وسائط داخل المسارات , فإنها هي التي تتأثر به

## الخيارات

### -d
لحذف الدلائل و الملفات الغير مستكشفة . اذا تمت ادارة الدليل الغير مستكشف من طرف مستودع " جيت" مختلف فإنه لن يحذف افتراضيا 
استخدم هذا الخيار مرتين اذا كنت تريد حذف مثل هذا الدليل 

<!--DOCUSAURUS_CODE_TABS-->
<!--الأمر-->
```bash
-f
```
<!--END_DOCUSAURUS_CODE_TABS-->
### -f
هذا الامر يوضع لجعل الاوامر تمر بدون تجاهلها او منعها حتى وان كان بها خطأ

### -i
اظهار ما يمكن القيام به وتنظيف الملفات بشكل تفاعلي

### -n
لا تقم بحذف اي شيء , اظهر فقط ما سيتم فعله 

### -q
اعرض فقط الاخطاء ولا شيء آخر 

### -e
 بالإضافة الى تلك الانماط الموجودة ضع في اعتبارك هذه الانماط في مجموعة قواعد التجاهل
 
### -x
 يمكن استخدام هذا (ربما بالتزامن مع إعادة تعيين "الجيت" ) لإنشاء دليل عمل أصلي لاختبار بنية نظيفة.

### -X
إزالة الملفات التي تجاهلها "الجيت" فقط. قد يكون هذا مفيدًا لإعادة إنشاء كل شيء من البداية ، ولكن الاحتفاظ بالملفات التي تم إنشاؤها يدويًا.


## الوضع التفاعلي
عندما يدخل الأمر في الوضع التفاعلي ، فإنه يعرض الملفات والدلائل المراد تنظيفها ، ويدخل في حلقة الأوامر التفاعلية الخاصة به.

تُظهر حلقة الأوامر قائمة الأوامر الفرعية المتاحة ، وتعطي مطالبة "ماذا الآن>". بشكل عام ، عندما تنتهي المطالبة بحرف واحد > ، يمكنك اختيار واحد فقط من الخيارات المعطاة ونوع العائد ، مثل هذا:

<!--DOCUSAURUS_CODE_TABS-->
<!--الأمر-->
```bash
    *** Commands ***
	1: clean                2: filter by pattern    3: select by numbers
	4: ask each             5: quit                 6: help
    What now> 1
```
<!--END_DOCUSAURUS_CODE_TABS-->


و توجد الكثير من الاومر في حلقة الاوامر منها 

### clean 
ابدء تنظيف الملفات والدلائل ، ثم قم بإنهاء

### filter by pattern
هذا يعرض الملفات والدلائل المراد حذفها ويصدر رسالة "تجاهل أنماط المدخلات >>". يمكنك إدخال أنماط مفصولة بمسافة لاستبعاد الملفات والدلائل من الحذف. عندما تكون راضيًا عن النتيجة التي تمت تصفيتها ، اضغط على رز الدخول (فارغ) مرة أخرى إلى القائمة الرئيسية.

### select by numbers
يعرض هذا الملفات والدلائل المراد حذفها ويصدر مطالبة "تحديد العناصر المراد حذفها >>". عندما تنتهي المطالبة بمضاعفة >> مثل هذا ، يمكنك إجراء أكثر من اختيار ، متصلاً بمسافة بيضاء أو فاصلة. كما يمكنك أن تقول النطاقات. مثلا "2-5 7،9" لاختيار 2،3،4،5،7،9 من القائمة. إذا تم حذف الرقم الثاني في نطاق ما ، فسيتم تحديد جميع العناصر المتبقية. مثلا "7-" لاختيار 7،8،9 من القائمة. يمكنك القول * لاختيار كل شيء. أيضًا عندما تكون راضيًا عن النتيجة التي تمت تصفيتها ، اضغط مفتاح "الإدخال" (فارغ) مرة أخرى إلى القائمة الرئيسية.

### ask each
سيبدأ هذا التنظيف ، ويجب عليك تأكيد واحداً تلو الآخر لحذف العناصر. يرجى ملاحظة أن هذا الإجراء غير فعال مثل الإجراءين أعلاه.

### quit
هذا يتيح لك الخروج دون تنظيف

### help 
عرض استخدام موجز للتفاعل 
git-clean
الخيارات
