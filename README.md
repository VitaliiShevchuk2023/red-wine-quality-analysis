
# Red Wine Quality Forecasts using Machine Learning Google Colab
https://sites.google.com/view/vinegarhill-datalabs/introduction-to-machine-learning/machine-learning-and-vinho-verde
https://colab.research.google.com/drive/1_64Ab7wNsVxvru-EbT8boiOOw1ltn7jk?usp=sharing

https://colab.research.google.com/drive/1Weap3SWDR6AlF9WJbl_KhpYxu07CBrh7?usp=sharing




# Vinho Verde: Унікальне португальське вино

## Експортний потенціал Португалії

- **Частка ринку:** 3,17% світового експорту вина у 2005 році
- **Зростання експорту Vinho Verde:** 36% між 1997 та 2007 роками

## Особливості Vinho Verde

### Унікальність найменування
- Термін стосується і стилю вина, і регіону походження
- **Вимова:** "вінью верде" (не "вінью вердей")

### Географія регіону
- Найбільший виноробний регіон Португалії
- Простягається до іспанського кордону на півночі
- Межує з Атлантичним океаном на заході
- Єдиний винний регіон у світі, який не названий на честь конкретного місця

## Кліматичні особливості

- Прохолодний та вологий клімат
- Вина з високою кислотністю
- Низький вміст алкоголю
- Призначені для вживання молодими

## Сертифікація та оцінка якості

### Значення контролю якості
- Запобігання незаконній фальсифікації
- Гарантування високих стандартів виробництва
- Підвищення якості виноробства

### Методи оцінки
1. **Фізико-хімічні тести**
   - Вимірювання густини
   - Аналіз вмісту алкоголю
   - Визначення рівня pH

2. **Сенсорні тести**
   - Базуються на експертній оцінці
   - Доповнюють лабораторні дослідження

### Процес тестування
- Автоматизована система iLab
- Повний цикл від запиту виробника до аналізу

## Практичне значення
- Стратифікація вин
- Визначення преміальних брендів
- Формування ціноутворення

## Джерела інформації
- [Olive Magazine](https://www.olivemagazine.com/drink/portuguese-vinho-verde-wine-guide/)
- [Wine Folly](https://winefolly.com/deep-dive/vinho-verde-the-perfect-poolside-wine-from-portugal/)
- [Наукова стаття](https://www.sciencedirect.com/science/article/abs/pii/S0167923609001377)




# Набір даних про якість червоного вина

## Джерело даних

Набір даних про якість червоного вина доступний у репозиторії машинного навчання UCI (Каліфорнійський університет в Ірвайні). Зразки червоного вина були зібрані з північної частини Португалії з метою моделювання якості вина на основі фізико-хімічних випробувань.

## Характеристики набору даних

- **Загальна кількість спостережень:** 1 599
- **Загальна кількість змінних:** 12

## Контекст та значимість дослідження

### Мета дослідження
- Запобігання незаконної фальсифікації вина
- Забезпечення контролю якості
- Вдосконалення виробництва вина

### Методологія тестування

#### Фізико-хімічні лабораторні тести
До випробувань входять визначення:
- Густини
- Вмісту алкоголю
- Рівня pH

#### Сенсорні тести
- Базуються на експертній оцінці
- Передбачають human intervention

### Процес реєстрації даних

Дані реєструвалися комп'ютеризованою системою (iLab), яка автоматизує процес тестування зразків вина:
- Від запиту виробника
- До лабораторного та сенсорного аналізу

## Технічні бібліотеки для аналізу даних

Для роботи з набором даних використовуються бібліотеки машинного навчання з Python:

- `sklearn.ensemble`:
  * RandomForestClassifier
  * GradientBoostingClassifier

- `sklearn.svm`:
  * SVC
  * LinearSVC

- `sklearn.linear_model`:
  * SGDClassifier
  * LogisticRegression

- `sklearn.preprocessing`:
  * StandardScaler
  * LabelEncoder

- `sklearn.model_selection`:
  * train_test_split
  * GridSearchCV
  * cross_val_score
  * StratifiedKFold

- `sklearn.neighbors`:
  * KNeighborsClassifier

- `sklearn.naive_bayes`:
  * GaussianNB

- `sklearn.metrics`:
  * confusion_matrix
  * classification_report
  * accuracy_score

## Додаткова інформація

- **Джерело даних:** Репозиторій UCI
- **Додаткові матеріали:** 
  * Сайт з даними: http://www3.dsi.uminho.pt/pcortez/wine/
  * Наукова стаття: https://www.sciencedirect.com/science...
 


# Аналіз якості червоного вина за допомогою машинного навчання

## Вступ до набору даних

### Характеристика набору даних
- Португальський набір даних про вино
- Загальна кількість спостережень: 1 599
- Шкала якості: від 3 до 8 балів
- Середній бал якості: 5.63

## Дослідження змінних

### Фізико-хімічні характеристики
1. **Алкоголь**
   - Відсоток алкоголю у вині
   - Позитивно корелює з якістю вина

2. **Леткa кислотність**
   - Пов'язана зі смаком оцту
   - Негативно корелює з якістю вина

3. **Інші важливі змінні**
   - Лимонна кислота
   - Сульфати
   - Щільність
   - Фіксована кислотність
   - Залишковий цукор

## Попередній аналіз даних

### Розподіл якості вина
- Більшість зразків мають бали 5-6
- Невелика кількість високоякісних зразків (7-8 балів)
- Мало низькоякісних зразків

### Кореляційний аналіз
- Позитивні кореляції:
  * Якість та алкоголь
  * Якість та сульфати
  * Якість та лимонна кислота
- Негативні кореляції:
  * Якість та летка кислотність

## Підготовка даних для машинного навчання

### Бінаризація якості
- Поділ на "хорошу" (> 6.5) та "погану" (≤ 6.5) якість
- Перетворення на бінарну класифікаційну задачу

### Розділення даних
- 80% для навчання
- 20% для тестування
- Стандартизація змінних

## Алгоритми машинного навчання

### Випробувані моделі
1. Випадковий ліс (Random Forest)
2. Наївний байєсівський класифікатор
3. Метод опорних векторів
4. К-найближчих сусідів
5. Логістична регресія

### Результати класифікації
- Висока точність передбачення
- Складність передбачення високоякісних зразків
- Найкраще працює випадковий ліс

## Особливості аналізу

### Виклики
- Дисбаланс класів
- Обмежена кількість високоякісних зразків
- Ризик "сліпого" передбачення

### Перспективи
- Автоматизація оцінки якості вина
- Можливість масштабування з більшими наборами даних

## Висновок

Машинне навчання надає потужний інструмент для аналізу якості вина, дозволяючи:
- Виявляти закономірності
- Передбачати якість
- Розуміти впливові фактори виробництва




# Резюме проекту: Прогнозування якості вина за допомогою машинного навчання

## Мета проекту
Розробка автоматизованої системи оцінки якості вина з використанням машинного навчання для оптимізації процесів wine-індустрії.

## Ключові аспекти дослідження

### Проблематика
- Традиційне тестування вина є:
  * Часномістким
  * Витратним
  * Пов'язаним з ризиками для дегустаторів

### Методологія
- Використано машинне навчання для аналізу якості вина
- Досліджено два набори даних: білі та червоні вина
- Проаналізовано 12 ключових атрибутів вина

## Технічні деталі

### Використані алгоритми
1. Логістична регресія
2. Випадковий ліс (Random Forest)
3. Градієнтний бустинг
4. Екстремальний градієнтний бустинг
5. K-найближчих сусідів (KNN)

### Підготовка даних
- Перевірка та очищення даних
- Стандартизація
- Розподіл на навчальну (80%) та тестову (20%) вибірки

## Результати

### Точність алгоритмів
- Логістична регресія: 55,7%
- Випадковий ліс: 
  * Білі вина: 96,83%
  * Червоні вина: 97,8%
- Інші алгоритми: близько 96%

### Найвпливовіші фактори
1. Залишковий цукор
2. Вміст алкоголю
3. Щільність

## Висновок
**Рекомендований алгоритм:** Випадковий ліс (Random Forest)

### Переваги підходу
- Висока точність прогнозування
- Швидкість аналізу
- Мінімізація ризиків у wine-індустрії

## Практичне значення
- Автоматизація оцінки якості вина
- Підтримка прийняття рішень у ви


# Кореляційний аналіз та викиди в наборі даних про вино

## Характеристика набору даних
- **Загальна кількість зразків:** 4 898
- **Кількість змінних:** 12 атрибутів

## Аналіз викидів

### Методологія виявлення викидів
- Використано графічний аналіз
- Перевірка outliers у всіх змінних
- **Результат:** Жодних викидів не виявлено

### Особливості дослідження
- Візуальний аналіз розподілу даних
- Перевірка екстремальних значень
- Збереження цілісності набору даних

## Кореляційний аналіз

### Методи дослідження
1. Таблиця кореляцій
2. Теплова карта (Heat Map)

### Ключові спостереження
- **Найвища кореляція:** Загальний діоксид сірки
- Мета дослідження: Виключити змінну з надмірною кореляцією

### Важливі змінні
1. Залишковий цукор
2. Алкоголь
3. Щільність

## Графічний аналіз взаємозв'язків

### Взаємозв'язок атрибутів
- Аналіз зв'язку між якістю та:
  * Вмістом алкоголю
  * Іншими фізико-хімічними показниками

### Ключові висновки
- Позитивна кореляція між якістю та вмістом алкоголю
- Складні нелінійні залежності між змінними

## Підготовка даних

### Етапи обробки
1. Перевірка на відсутні значення
2. Видалення змінних з надмірною кореляцією
3. Стандартизація даних
4. Розподіл на навчальну та тестову вибірки

### Важливі рішення
- Видалення стовпця якості як цільової змінної
- Бінаризація якості (значення > 7 як "хороша")

## Висновок
Ретельний кореляційний аналіз дозволив:
- Очистити набір даних
- Виявити ключові змінні
- Підготувати дані для машинного навчання


---------------------------------------------------------------------------------
Project 6. Wine Quality Prediction using Machine Learning with Python | Machine Learning Project, https://www.youtube.com/watch?v=CBxJuwrGrc4



# Прогнозування якості вина за допомогою машинного навчання

## Вступ до проекту

### Мета дослідження
- Створення системи оцінки якості вина
- Використання машинного навчання для аналізу хімічних параметрів
- Автоматизація процесу визначення якості вина

## Проблематика

### Виклики wine-індустрії
- Традиційне тестування вина:
  * Тривале
  * Витратне
  * Пов'язане з ризиками для дегустаторів

### Інноваційне рішення
- Застосування машинного навчання
- Швидкий аналіз хімічних параметрів
- Об'єктивна оцінка якості

## Workflow проекту

### Основні етапи
1. Імпорт залежностей
2. Збір даних
3. Аналіз даних
4. Попередня обробка даних
5. Розділення на навчальну та тестову вибірки
6. Навчання моделі
7. Оцінка результатів
8. Створення передбачувальної системи

## Технічні інструменти

### Бібліотеки
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

### Алгоритм машинного навчання
- Випадковий ліс (Random Forest)
- Ансамблева модель на основі дерев рішень

## Аналіз даних

### Дослідження параметрів
- Фіксована кислотність
- Летка кислотність
- Лимонна кислота
- Залишковий цукор
- Хлориди
- Діоксид сірки
- Щільність
- pH
- Сульфати
- Вміст алкоголю

### Кореляційний аналіз
- Виявлення зв'язків між параметрами
- Визначення впливу на якість вина

## Підготовка даних

### Попередня обробка
- Перевірка на відсутні значення
- Бінаризація міток
- Розподіл на навчальну (80%) та тестову (20%) вибірки

## Навчання моделі

### Випадковий ліс (Random Forest)
- Ансамблева модель дерев рішень
- Механізм:
  * Створення множини дерев рішень
  * Колективне голосування
  * Підвищення точності прогнозування

### Результати
- Точність моделі: 93%
- Висока ефективність передбачення якості вина

## Передбачувальна система

### Функціональність
- Прийом хімічних параметрів
- Передбачення якості вина
- Бінарна класифікація (добра/погана якість)

## Висновки

### Переваги підходу
- Швидкість аналізу
- Об'єктивність оцінки
- Мінімізація людського фактору
- Потенціал для масштабування

### Подальші перспективи
- Вдосконалення моделі
- Розширення параметрів аналізу
- Інтеграція в wine-індустрію

-------------------------------------------------------------------







Посилання: 

- Red Wine Quality Analysis and Machine Learning Techniques using sklearn python libraries, https://www.youtube.com/watch?v=lHwESP3-Efg
- PREDICTION OF WINE QUALITY USING MACHINE LEARNING, https://www.youtube.com/watch?v=vGvGakmABVA
- Mastering Wine Quality Prediction: Implementation of Decision Tree Algorithm, https://www.youtube.com/watch?v=7mQHfZDykY0
- Red Wine Quality Classification Project | Machine Learning | Python, https://www.youtube.com/watch?v=1tiK-HSGbOA
- Project 6. Wine Quality Prediction using Machine Learning with Python | Machine Learning Project, https://www.youtube.com/watch?v=CBxJuwrGrc4
- Red Wine Quality Prediction | Kaggle Dataset | Machine Learning | Logistic | Decision | RandomForest, https://www.youtube.com/watch?v=jzH4MCvnto4
- 
  


  # MACHINE LEARNING PROJECTS
  https://www.youtube.com/playlist?list=PL_1pt6K-CLoDcWw_c196kZn7aPeLdRDOU
  
-  Project 1 Addition of Two Numbers End-To-End Machine Learning Project, https://www.youtube.com/watch?v=qX1NJfrAM8A&list=PL_1pt6K-CLoDcWw_c196kZn7aPeLdRDOU
-  Project 2 Health Insurance Cost Prediction End To End Machine Learning Project | Part 1, https://www.youtube.com/watch?v=eshMzk8L3ic&list=PL_1pt6K-CLoDcWw_c196kZn7aPeLdRDOU&index=2
-  Project - 2 Build Data Machine Learning Web App Using Python & Streamlit | Part 2, https://www.youtube.com/watch?v=Hn_HXPyCvSI&list=PL_1pt6K-CLoDcWw_c196kZn7aPeLdRDOU&index=3
-  Project - 2 Deploy Machine Learning Streamlit Web App on Heroku Cloud | Part 3, https://www.youtube.com/watch?v=7tT0o2koaaA&list=PL_1pt6K-CLoDcWw_c196kZn7aPeLdRDOU&index=4
-  Develop Android Application For Machine Learning Projects | Project - 2, https://www.youtube.com/watch?v=GLGIPnTb018&list=PL_1pt6K-CLoDcWw_c196kZn7aPeLdRDOU&index=5
     
