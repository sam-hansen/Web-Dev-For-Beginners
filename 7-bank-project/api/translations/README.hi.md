# बैंक एपीआई

> [नोडजेयस](https://nodejs.org) + [एक्सप्रेस](https://expressjs.com/) के साथ बनाया गया बैंक एपीआई.

एपीआई आपके लिए पहले से ही बनाया गया है और व्यायाम का हिस्सा नहीं है.

हालाँकि, अगर आप यह जानने के लिए इच्छुक हैं कि एपीआई कैसे बनाया जाए तो आप इस वीडियो की श्रृंखला का अनुसरण कर सकते हैं: https://aka.ms/NodeBeener (वीडियो 17 से 21 के माध्यम से इस सटीक एपीआई कवर करता है).

आप इस इंटरेक्टिव ट्यूटोरियल पर भी नज़र डाल सकते हैं: https://aka.ms/learn/express-api

## सर्वर चल रहा है

सुनिश्चित करें कि आपके पास [नोडजेयस](https://nodejs.org) स्थापित है.

1. ये गिट रेपो क्लोन करे.
2. `api` फ़ोल्डर में एक टर्मिनल खोलें, फिर `npm install` चलाएं.
3. `npm start` चलाए.

सर्वर को `5000` पोर्ट पर सुनना शुरू करना चाहिए.

> नोट: सभी प्रविष्टियों को मेमोरी में संग्रहीत किया जाता है और उन्हें बनाए नहीं रखा जाता है, इसलिए जब सर्वर बंद हो जाता है तो सभी डेटा खो जाता है.

## एपीआई विवरण

| रूट                                         | विवरण                                                                                                       |
| ------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| GET /api/                                   | सर्वर जानकारी प्राप्त करें                                                                                  |
| POST /api/accounts/                         | एक खाता बनाएँ, उदाहरण के लिए: `{ user: 'Yohan', description: 'My budget', currency: 'EUR', balance: 100 }`  |
| GET /api/accounts/:user                     | निर्दिष्ट खाते के लिए सभी डेटा प्राप्त करें                                                                 |
| DELETE /api/accounts/:user                  | निर्दिष्ट खाता हटाए                                                                                         |
| POST /api/accounts/:user/transactions       | एक लेनदेन जोड़े, उदाहरण के लिए: `{ date: '2020-07-23T18:25:43.511Z', object: 'Bought a book', amount: -20 }` |
| DELETE /api/accounts/:user/transactions/:id | निर्दिष्ट लेनदेन हटाए                                                                                       |
