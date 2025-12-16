# Heart Disease Cleveland UCI: An End-to-End Machine Learning Project

## Project Overview
This project presents an end-to-end machine learning pipeline for predicting the
presence of heart disease using the Heart Disease Cleveland UCI dataset. The main
objective is to build a reliable and medically meaningful classification model
that prioritizes the detection of patients with heart disease.

Unlike projects that focus solely on accuracy, this work emphasizes recall and
the reduction of missed disease cases, which is a critical requirement in
medical decision-support systems.

---

## Dataset
- **Name:** Heart Disease Cleveland UCI
- **Samples:** 303 patient records
- **Features:** Clinical and demographic attributes
- **Target Variable:**  
  - `condition = 0` → No heart disease  
  - `condition = 1` → Presence of heart disease

---

## Methodology

### 1. Exploratory Data Analysis (EDA)
- Analysis of feature distributions
- Correlation analysis between clinical variables
- Identification of relationships with the target variable
- Data cleaning and preparation

> The EDA phase was completed in a previous project and this notebook builds
directly on the prepared dataset.

---

### 2. Machine Learning Models

#### Baseline Model
- **Logistic Regression**
- Feature scaling applied using standardization
- Used as a reference point for performance evaluation

#### Model Improvement
- Class weighting applied to give higher importance to positive cases
- Decision threshold adjusted to improve disease detection
- Focus placed on reducing false negative predictions

#### Alternative Model
- **Decision Tree Classifier**
- Multiple tree depths tested to evaluate performance
- Increased complexity did not lead to improved medical performance

---

## Model Evaluation
The models were evaluated using:
- Confusion Matrix
- Recall (Sensitivity)
- Precision
- Classification Report

Special emphasis was placed on recall, as missing a positive heart disease case
can have serious medical consequences.

---

## Final Model Selection
The final selected model is:
- **Logistic Regression with class weighting and a custom decision threshold**

This model was chosen due to:
- High recall in detecting heart disease cases
- Reduced number of false negatives
- Model stability and simplicity
- Interpretability, which is essential in medical applications

---

## Key Takeaways
- Accuracy alone is not sufficient for evaluating medical models
- Model selection must consider the cost of different types of errors
- Simpler, well-tuned models can outperform more complex models in real-world scenarios

---

## Tools and Libraries
- Python
- Numpy, Pandas
- matplotlib, seaborn
- Scikit-learn (for -> LabelEncoder، StandardScaler، MinMaxScaler)
- scipy (for -> stats, chi2_contingency, ttest_ind, shapiro)
- statsmodels (for ->  ols, sm, pairwise_tukeyhsd)

---

## Author
Mosab Osama

This project is intended for educational and portfolio purposes and demonstrates
a practical approach to applying machine learning in healthcare-related problems.


___________________________________________________________________________________________________________________


# Heart Disease Cleveland UCI: مشروع تعلّم آلة متكامل من البداية إلى النهاية

## نظرة عامة على المشروع
يعرض هذا المشروع خط أنابيب متكامل لتعلّم الآلة يهدف إلى التنبؤ بوجود أمراض
القلب باستخدام بيانات Heart Disease Cleveland UCI. يركّز المشروع على بناء
نموذج تصنيف موثوق وذو معنى طبي، مع إعطاء أولوية لاكتشاف الحالات المرضية.

على عكس المشاريع التي تعتمد فقط على مقياس الدقة، يركّز هذا العمل على مقياس
الاستدعاء وتقليل عدد الحالات المرضية التي لا يتم اكتشافها، وهو مطلب أساسي
في أنظمة دعم القرار الطبي.

---

## مجموعة البيانات
- **الاسم:** Heart Disease Cleveland UCI
- **عدد العينات:** 303 سجلًا للمرضى
- **الخصائص:** متغيرات سريرية وديموغرافية
- **المتغير الهدف:**  
  - `condition = 0` → لا يوجد مرض في القلب  
  - `condition = 1` → وجود مرض في القلب

---

## المنهجية

### 1. التحليل الاستكشافي للبيانات
- تحليل توزيع الخصائص
- دراسة الارتباطات بين المتغيرات السريرية
- فهم العلاقة مع المتغير الهدف
- تنظيف البيانات وتجهيزها

> تم تنفيذ مرحلة التحليل الاستكشافي للبيانات في مشروع سابق، ويعتمد هذا
المشروع مباشرة على البيانات المجهزة.

---

### 2. نماذج تعلّم الآلة

#### النموذج الأساسي
- نموذج الانحدار اللوجستي
- تطبيق مقياس التوحيد على البيانات
- استخدامه كنقطة مرجعية لتقييم الأداء

#### تحسين النموذج
- تطبيق أوزان للفئات لإعطاء أهمية أكبر للحالات المرضية
- تعديل عتبة اتخاذ القرار لزيادة قدرة النموذج على اكتشاف المرض
- التركيز على تقليل الحالات السلبية الكاذبة

#### نموذج بديل
- نموذج شجرة القرار
- اختبار أعماق مختلفة للشجرة
- زيادة التعقيد لم تؤدِّ إلى تحسين الأداء الطبي

---

## تقييم النماذج
تم تقييم النماذج باستخدام:
- مصفوفة الارتباك
- مقياس الاستدعاء
- مقياس الدقة
- تقرير التصنيف

تم إعطاء أهمية خاصة لمقياس الاستدعاء نظرًا لخطورة إغفال الحالات المرضية في
السياق الطبي.

---

## اختيار النموذج النهائي
تم اختيار النموذج النهائي على النحو التالي:
- نموذج الانحدار اللوجستي مع وزن الفئات وتعديل عتبة اتخاذ القرار

ويرجع سبب الاختيار إلى:
- ارتفاع قدرة النموذج على اكتشاف الحالات المرضية
- تقليل عدد الحالات التي لم يتم اكتشافها
- استقرار النموذج وبساطته
- قابليته للتفسير، وهو أمر مهم في التطبيقات الطبية

---

## أهم الاستنتاجات
- لا يكفي الاعتماد على مقياس الدقة وحده في التطبيقات الطبية
- يجب أن يأخذ اختيار النموذج في الاعتبار تكلفة أنواع الأخطاء المختلفة
- النماذج البسيطة المضبوطة جيدًا قد تتفوق على النماذج الأكثر تعقيدًا

---

## الأدوات والمكتبات المستخدمة
- Python
- Numpy, Pandas
- matplotlib, seaborn
- Scikit-learn (for -> LabelEncoder، StandardScaler، MinMaxScaler)
- scipy (for -> stats, chi2_contingency, ttest_ind, shapiro)
- statsmodels (for ->  ols, sm, pairwise_tukeyhsd)

---

## الكاتب
مصعب أسامة

هذا المشروع مخصص للأغراض التعليمية وبناء السيرة الذاتية، ويعرض تطبيقًا عمليًا لتعلّم الآلة في مجال الرعاية الصحية.

