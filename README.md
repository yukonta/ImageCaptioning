# ImageCaptioning

Адрес проекта ImageCaptioning на гугл-диске: https://drive.google.com/drive/folders/1mTYLfMFt_G19LjLlx64Nk63fAOZJH6it?usp=sharing

Адрес каталога на гугл-диске с дополнительными БОЛЬШИМИ файлами, использующимися в ноутбуке опционально («captions» и пропущенные через энкодеры InceptionV3 и Resnet50 картинки, полученные из MSCOCO2017, Flickr30k, а также GoogleNews-vectors-negative300.bin - эмбеддинги из Word2Vec): https://drive.google.com/drive/folders/1Ifme0Q3MQkAFEdflop4HERpFnYEDqngW?usp=sharing. Перечень и инструкция по использованию файлов - в TableResults.docx. Ноутбук работает с датасетом MSCOCO2014 без этих дополнительных файлов. 

В этом репозитории размещены файлы:
1. yukonta_image_captionong.ipynb - ноутбук с выполненным заданием;

2. TableResults.docx  - файл с подробным описанием результатов экспериментов и .

Проводились эксперименты как в соответствии с базовой частью задания, так и с вариативной:

1) Сделан телеграм-бот  EasyCaption  – см. исходники на гитхабе : https://github.com/yukonta/EasyCaption

2) Использовались предобученные эмбеддинги  - из Word2Vec.

3) Эксперименты с двумя вариантами энкодера – InceptionV3 и Resnet50.

4) Эксперименты с тремя вариантами датасета: MSCOCO2014, MSCOCO2017, Flickr30k.

5) Эксперименты с Attention.

6) Различные гиперпараметры (batch_size, lr, emb_size), разное количество слоев LSTM (1, 2), разное количество конкатенированных LSTM (от 1 до 3), размер hidden и cell –векторов, lstm_dropout, различные значения clip для для torch.nn.utils.clip_grad_norm_, разные adam_weight_decay, динамически меняющийся lr.

7) EarlyStopping.

8) Графики train и val лоссов.
