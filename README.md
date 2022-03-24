# hse_hw3_chromhmm

## Colab

https://colab.research.google.com/drive/1miprpZod7uvntxQTSaEubEapmMsgNxbi?usp=sharing

## Выбранные данные

Клеточная линия: HelaS3.

| **Гистоновая метка** | H2AZ | H3K4me1 | H3K4me2 | H3K4me3 | H3K9ac | H3K9me3 | H3K27ac | H3K27me3 | H3K36me3 | H3K79me2 | H4K20me1 | Контроль |
| ------------- | ------------- |--------------------| -- | -- | -- | -- | -- | -- | -- | -- | -- | -- |
| **Название файла** | H2AZ.bam | H3k04me1.bam | H3k04me2.bam | H3k04me3.bam | H3k09ac.bam | H3k09me3.bam | H3k27ac.bam | H3k27me3.bam | H3k36me3.bam | H3k79me2.bam | H4k20me1.bam | ControlStdAlnRep1.bam |


## Результаты

### Картинки из выдачи ChromHMM

| ![image](https://github.com/shaggy99999/hse_hw3_chromhmm/blob/main/results%2010/Helas3_10_RefSeqTES_neighborhood%20(1).png) | ![image](https://github.com/shaggy99999/hse_hw3_chromhmm/blob/main/results%2010/Helas3_10_RefSeqTSS_neighborhood.png) | ![image](https://github.com/shaggy99999/hse_hw3_chromhmm/blob/main/results%2010/Helas3_10_overlap.png) | ![image](https://github.com/shaggy99999/hse_hw3_chromhmm/blob/main/results%2010/emissions_10.png) | ![image](https://github.com/shaggy99999/hse_hw3_chromhmm/blob/main/results%2010/transitions_10.png) |
| ------------- | ------------- |--------------------| -- | -- |

### Скриншоты из геномного браузера

![image](https://user-images.githubusercontent.com/93095449/158063953-2923a847-c649-4a20-9c94-1fa60ee7ad98.png)

![image](https://user-images.githubusercontent.com/93095449/158064187-1505fe47-9cea-4682-b391-0bd07b049e28.png)

![image](https://user-images.githubusercontent.com/93095449/158064258-dfe01fe2-7b8d-4271-a4bd-2585fbdadbe2.png)

### Выводы
CPGisland чаще всего находиться в состоянии 1, в геномном браузере состояние 1 синего цвета-этот цвет ассоциируется с островками которые чаще всего распологаются в ядерной ламине

| **Состояние** | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
| ------------- | ------------- |--------------------| -- | -- | -- | -- | -- | -- | -- | -- |
<!-- | **Частые гистоновые метки** | H2AZ, H3K27ac, H3K9ac, H3K4me3, H3K4me2, H3K4me1, H3K79me2 | H2AZ, H3K27ac, H3K9ac, H3K4me3, H3K4me2, H3K4me1 | H3K4me1 | H3K4me2, H3K79me2 (H3K27ac, H3K9ac, H3K4me3, H3K4me1) | H3K79me2 (H3K4me1, H4K20me1, H3K36me3) | H3K79me2,  H4K20me1, H3K36me3 | H4K20me1 | H2AZ, H4K20me1, H3K9me3 (H3K9ac, H3K79m2, H3K27me3) | H4K20me1, H3K27me3 | H3K36me3, H3K79me2, H4K20me1 | 
| **В каких частях генома расположены** | Ядерная ламина | Ядерная ламина, много в геноме | Ядерная ламина (конец транскрипции, экзоны) | Конец транскрипции, гены, экзоны | Гены (конец транскрипции, экзоны) | Гены, конец транскрипции (экзоны) | Ядерная ламина, конец транскрипции | Примерно равное распределение по всем категориям | CpG, экзоны, старт транскрипции | Конец транскрипции, гены, экзоны |
| **Какие состояния расположены рядом с этим** | 2 | - | 2 | - | 4, 6 | 5, 10, 4 | 2, 8 | 7, 9, 2, 1 | 8, 10 | 6, 9 |
| **Расположение относительно старта транскрипции** | - | - | - | - | - | (до и после TSS) | (до TSS) | На TSS (до TSS) | На TSS и по обе стороны | (До) и после TSS |
| **Расположение относительно конца транскрипции** | (До, на и после TES) | - | (До, на и после TES) | До, на и после TES | (До и на TES) | (До, на и после TES) | (После TES) | (До, на и после TES) | До (на и после TES) | До, на (и после TES) |
| **Вывод** | Polycomb-repressed | Heterochromatin 1 | Heterochromatin 2 | Transcribed region 1 | Transcribed region 2 | Transcribed region/Enhancer | Enhancer | Enhancer 2 | Active promoter | Weak promoter |

### Скриншоты бонусной части

![image](https://user-images.githubusercontent.com/93095449/158068403-294baec3-965b-4b3c-bca6-cdae5fb7a17d.png)

![image](https://user-images.githubusercontent.com/93095449/158068444-f36b9d8d-570a-4b2d-bbbf-122964768219.png)

Как я это сделал? Открыл '...dense.bed' в Notepad++ и заменил номера состояний на соответствующие названия 
