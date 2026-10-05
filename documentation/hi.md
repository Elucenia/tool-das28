<!-- ELUCENIA technical documentation · das28 · hi · no clinical/professional/rights approval -->

# DAS28 (ESR और CRP)

[शर्तें, स्रोत और अनुमतियाँ](https://elucenia.org/hi/tools/das28)

## उपयोग कैसे करें

पोर्टल पर उपकरण का उपयोग करें या स्थानीय HTTP सर्वर के माध्यम से index.html खोलें। भाषा चुनें, फ़ील्ड भरें और गणना करें।

## इनपुट और इकाइयाँ

### दर्द वाले जोड़ (28 में से)

`tjc`

सीमा: 0–28

### सूजे हुए जोड़ (28 में से)

`sjc`

सीमा: 0–28

### रोगी द्वारा समग्र स्वास्थ्य आकलन (दृश्य स्केल)

`gh`

mm · सीमा: 0–100

### एरिथ्रोसाइट सेडिमेंटेशन दर (ESR)

`vhs`

mm/h · वैकल्पिक · सीमा: 1–150

### सी-रिएक्टिव प्रोटीन (CRP)

`pcr`

mg/L · वैकल्पिक · सीमा: 0–300

## विधि का संस्करण

DAS28-ESR/Prevoo 1995 और DAS28-CRP/Wells 2009; 28 जोड़; CRP इंटरसेप्ट 0.96

## दस्तावेज़ित सूत्र

DAS28-ESR = 0.56 × √(दर्दयुक्त) + 0.28 × √(सूजे हुए) + 0.70 × ln(ESR) + 0.014 × समग्र आकलन.

DAS28-CRP = 0.56 × √(दर्दयुक्त) + 0.28 × √(सूजे हुए) + 0.36 × ln(CRP + 1) + 0.014 × समग्र आकलन + 0.96 (CRP mg/L में).

## सीमाएँ और जनसमूह

DAS28 को 1995 में रुमेटॉइड आर्थराइटिस की गतिविधि के लिए विकसित किया गया था; इसमें 28 जोड़ों की गिनती और रुमेटोलॉजिस्ट के नैदानिक आकलन से तुलना इस्तेमाल हुई। C-रिएक्टिव प्रोटीन (CRP) वाला रूप अपने आप एरिथ्रोसाइट अवसादन दर (ESR) वाले रूप के समान नहीं है; सूत्र, इकाइयाँ और कट-ऑफ प्रयुक्त स्रोत और संस्करण से मेल खाने चाहिए।

## संदर्भ

- [Prevoo MLL et al. Modified disease activity scores that include twenty-eight-joint counts: development and validation in a prospective longitudinal study of patients with rheumatoid arthritis. Arthritis Rheum, 1995.](https://doi.org/10.1002/art.1780380107)

- [Wells G et al. Validation of the 28-joint Disease Activity Score (DAS28) and European League Against Rheumatism response criteria based on C-reactive protein against disease progression in patients with rheumatoid arthritis, and comparison with the DAS28 based on erythrocyte sedimentation rate. Ann Rheum Dis, 2009.](https://doi.org/10.1136/ard.2007.084459)

- [England BR et al. 2019 Update of the American College of Rheumatology Recommended Rheumatoid Arthritis Disease Activity Measures. Arthritis Care Res, 2019.](https://doi.org/10.1002/acr.24042)

## तकनीकी परीक्षण दोहराएँ

दर्ज कृत्रिम मामलों को दोहराने के लिए इस रिपॉज़िटरी की मूल निर्देशिका में node test.cjs चलाएँ। मूल इनपुट, अपेक्षित परिणाम और सहनशीलता सीमाएँ सुरक्षित रखी गई हैं। तकनीकी परीक्षण नैदानिक सत्यापन नहीं हैं।

```sh
node test.cjs
```

tool.json में स्रोत, संस्करण और समीक्षा का दायरा दिया गया है। examples.json में कृत्रिम इनपुट और अपेक्षित परिणाम सुरक्षित हैं; results.json में प्राप्त परिणाम दर्ज हैं।

[रिकॉर्ड और संदर्भ](../tool.json) · [JavaScript कोड](../calculator.js) · [संदर्भ मामले](../examples.json) · [results.json](../results.json)

## समीक्षा और उपयोग की शर्तें

स्वतंत्र नैदानिक समीक्षा नहीं की गई है।

यह इंटरफ़ेस लेखकों द्वारा किया गया अनुवाद है, कोई आधिकारिक या प्रमाणित संस्करण नहीं। स्वतंत्र नैदानिक समीक्षा, पेशेवर भाषाई समीक्षा और उपकरणों के अधिकारों की अनुमति की प्रक्रिया पूरी नहीं हुई है।

सूत्र या वर्गीकरण का परिणाम। व्याख्या, कार्यवाही और उपयुक्तता पेशेवर मूल्यांकन और चुने गए स्रोत पर निर्भर है।

## लाइसेंस और श्रेय

Apache-2.0 केवल ELUCENIA के कोड पर लागू होता है। उपकरणों, प्रकाशनों, अनुवादों और डेटा के अधिकार उनके संबंधित अधिकारधारकों के पास रहते हैं। LICENSE और NOTICE सुरक्षित रखें।

ELUCENIA · Felipe Guedes · Copyright © 2026
