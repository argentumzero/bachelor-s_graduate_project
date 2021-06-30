# bachelor-s_graduate_project
Hello, my name is Nalimova Elizaveta Alekseevna. I am 21 years old. I have bachelor's degree in specialty "Information Security".
My graduation project was named "Information security incident managment based on artifical intellegence methods". I'll be honest, the title doesn't match with content.
The dicrepancy is due to tight deadlines and the fact that I was alone development. I wanted to develop system similar to SIEM. But I overestimated my capabilities, only incident
response was implemented in my project. I tried to compensate for this shortcoming with my research and achieved little success.
Project discription:
1. I had raw JSON files with malware signatures in the form of messages from antivirus and network traffic in the form Wireshark files (.pcap).
I prepared the data like this: extracting signatures from files, creating fixed strings and poisoning them with virus signatures, this is how synthetic viruses were created.
Network traffic was divided into clean and abnormal, to simplify the work, I assigned an abnormality coefficient to each metadata frame. Abnormal coefficient has high 
value, if frame contains abnormal metadata, and low value, if metadata is normal.
2. Convolutional neural network worked with synthetic viruses. Autoencoder based on long-short term memory worked with network traffic. 
I created 3 datasets for CNN: a training dataset, that tests for adequacy and a dataset that has no class markup. 
The processed dataset with network traffic was split into clean and abnormal datasets. The training took place on a clean dataset, and the autoencoder was checked on an abnormal dataset.
3. We got intermediate data. The two datasets have been merged into one. 
The data inside was translated into binary sequences, as in the classical classification problem for a multilayer perceptron.
4. I created two multilayer perceptrons, the first, based on a single dataset, 
gives an answer about the presence of an anomaly, the second determines which virus was detected. 
Training takes place on the transformed intermediate data. The work of the model is checked on a randomly generated dataset, which is similar to a training dataset.
5. I also created a dataset with response scripts. Models, after processing, return values that correspond to the script numbers. 

Здравствуй, меня зовут Налимова Елизавета Алексеевна. Мне 21 год. Я получила степень бакалавра по специальности "Информационная безопасность".
Моя выпускная квалификационная работа называется "Управление инцидентами информационной безопасности на основе методов искусственного интеллекта". Буду честна, 
название не совсем соответсвует содержанию. Это объясняется тем, что сроки были сжаты и я в одиночку занималась разработкой. Моей целью было создать систему, похожу на SIEM.
Однако я переоценила свои возможности, поэтому в проекте реализовано только реагирование. 
Я постаралась компенсировать этот недостаток исследованиями и достигла в этом небольшого успеха.
Описание проекта:
1. Изначально у меня были сырые JSON-файлы с сигнатурами малварей в виде сообщений от антивируса и сетевой трафик в виде файлов Wireshark.
Данные были преобразованы следующим образом: извлечены сигнатуры, созданы фиксированные строки и отравлены сигнатурами вирусов. Полученные записи были названы синтетическими вирусами.
Сетевой трафик был разделен на чистый и аномальный, для упрощения работы, каждому фрейму метаданных был присвоен коэффициент аномальности. Данный коэффициент имеет большое значение, 
если запись аномальна, и маленькое, если запись нормальная.
2. Сверочная нейронная сеть работает с синтетическими вирусами. Автоэнкодер на основе долгой краткосрочной памяти работает с сетевым трафиком. Было создано 3 датасета: обучающий,
проверяющий адекватность и датасет без классовой разметки. Обработанный датасет был разделен на чистый и аномальный. Обучение автоэнкодера происходит на чистых записях,
а проверка на аномальных.
3. Получены промежуточные данные. Два датасета объединены в один. Данные внутри подверглись преобразованию в бинарной последовательности, с результате они были сведены к датасету
как в классической задаче классификации многослойным персептроном.
4. Я создала 2 многослойных персептрона, первый, основываясь на едином датасете, определяет есть ли аномалия в сетевом трафике, второй определяет какой именно вирус 
был зарегестрирован. Обучение происходит на промежуточных данных. Сама модель работает на наборе данных, сгенерированном случайно, похожим на обучающий набор.
5. Так же был создан датасет, содержащий сценарии реагирования. Модели, после обработки, позвращают значение, соответсвующее номеру сценария.
