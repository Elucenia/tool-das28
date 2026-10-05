<!-- ELUCENIA technical documentation · das28 · ar · no clinical/professional/rights approval -->

# DAS28 (ESR وCRP)

[الشروط والمصادر والأذونات](https://elucenia.org/ar/tools/das28)

## كيفية الاستخدام

استخدم الأداة في البوابة أو افتح index.html عبر خادم HTTP محلي. اختر اللغة، وأكمل الحقول، ثم أجرِ الحساب.

## المدخلات والوحدات

### المفاصل المؤلمة (من ٢٨)

`tjc`

النطاق: ٠–٢٨

### المفاصل المتورمة (من ٢٨)

`sjc`

النطاق: ٠–٢٨

### تقييم المريض العام للصحة (مقياس بصري)

`gh`

mm · النطاق: ٠–١٠٠

### سرعة تثفل الكريات الحمراء (ESR)

`vhs`

mm/h · اختياري · النطاق: ١–١٥٠

### البروتين المتفاعل C (CRP)

`pcr`

mg/L · اختياري · النطاق: ٠–٣٠٠

## إصدار الطريقة

DAS28-ESR/بريفو 1995 وDAS28-CRP/ويلز 2009؛ 28 مفصلًا؛ ثابت CRP هو 0.96

## المعادلة الموثقة

DAS28-ESR = 0.56 × √(المؤلمة) + 0.28 × √(المتورمة) + 0.70 × ln(ESR) + 0.014 × التقييم العام.

DAS28-CRP = 0.56 × √(المؤلمة) + 0.28 × √(المتورمة) + 0.36 × ln(CRP + 1) + 0.014 × التقييم العام + 0.96 (CRP بوحدة mg/L).

## الحدود والفئة السكانية

طُوّر DAS28 عام 1995 لتقييم نشاط التهاب المفاصل الروماتويدي، باستخدام عدّ 28 مفصلًا ومقارنات بالتقييم السريري لأطباء الروماتيزم. نسخة البروتين المتفاعل C ‏(CRP) لا تكافئ تلقائيًا نسخة سرعة ترسيب كريات الدم الحمراء (ESR)؛ ويجب أن تتوافق المعادلة والوحدات والعتبات مع المصدر والنسخة المستخدمين.

## المراجع

- [Prevoo MLL et al. Modified disease activity scores that include twenty-eight-joint counts: development and validation in a prospective longitudinal study of patients with rheumatoid arthritis. Arthritis Rheum, 1995.](https://doi.org/10.1002/art.1780380107)

- [Wells G et al. Validation of the 28-joint Disease Activity Score (DAS28) and European League Against Rheumatism response criteria based on C-reactive protein against disease progression in patients with rheumatoid arthritis, and comparison with the DAS28 based on erythrocyte sedimentation rate. Ann Rheum Dis, 2009.](https://doi.org/10.1136/ard.2007.084459)

- [England BR et al. 2019 Update of the American College of Rheumatology Recommended Rheumatoid Arthritis Disease Activity Measures. Arthritis Care Res, 2019.](https://doi.org/10.1002/acr.24042)

## إعادة إجراء الاختبارات التقنية

شغّل node test.cjs في المجلد الجذري لهذا المستودع لتكرار الحالات الاصطناعية المسجلة. تُحفظ المدخلات والنتائج المتوقعة وحدود التفاوت الأصلية. لا تُعدّ الاختبارات التقنية تحققًا سريريًا.

```sh
node test.cjs
```

يحتوي tool.json على المصادر والإصدار ونطاق المراجعة. يحتفظ examples.json بالمدخلات والنتائج المتوقعة للحالات الاصطناعية؛ ويسجل results.json النتائج التي تم الحصول عليها.

[السجل والمراجع](../tool.json) · [شيفرة JavaScript](../calculator.js) · [حالات مرجعية](../examples.json) · [results.json](../results.json)

## المراجعة وشروط الاستخدام

لم تُجرَ مراجعة سريرية مستقلة.

هذه الواجهة ترجمة أعدّها مؤلفوها، وليست إصدارًا رسميًا أو معتمدًا. لم تُجرَ مراجعة سريرية مستقلة أو مراجعة لغوية مهنية، ولم تُستكمل الموافقة على حقوق استخدام الأدوات.

نتيجة المعادلة أو التصنيف. يعتمد التفسير والتصرف ومدى الانطباق على التقييم المهني والمصدر المحدد.

## الترخيص ونسبة العمل إلى أصحابه

ينطبق Apache-2.0 على كود ELUCENIA فقط. تبقى حقوق الأدوات والمنشورات والترجمات والبيانات لأصحابها المعنيين. احتفظ بملفّي LICENSE وNOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
