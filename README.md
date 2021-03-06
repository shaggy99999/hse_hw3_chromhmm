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

![image](https://github.com/shaggy99999/hse_hw3_chromhmm/blob/main/images/2022-03-24_16-10-09.png)

![image](https://github.com/shaggy99999/hse_hw3_chromhmm/blob/main/images/2022-03-24_16-45-21.png)

![image](https://github.com/shaggy99999/hse_hw3_chromhmm/blob/main/images/2022-03-24_16-46-44.png)

### Выводы


| **Состояние** | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
| ------------- | ------------- |--------------------| -- | -- | -- | -- | -- | -- | -- | -- |
| **Частые гистоновые метки** | H2AZ, H3K27ac, H3K9ac, H3K4me3, H3K4me2, H3K4me1, H3K79me2 | H2AZ, H3K27ac, H3K9ac, H3K4me3, H3K4me2, H3K4me1 | H3K4me1 | H3K4me2, H3K79me2 (H3K27ac, H3K9ac, H3K4me3, H3K4me1) | H3K79me2 (H3K4me1, H4K20me1, H3K36me3) | H3K79me2,  H4K20me1, H3K36me3 | H4K20me1 | H2AZ, H4K20me1, H3K9me3 (H3K9ac, H3K79m2, H3K27me3) | H4K20me1, H3K27me3 | H3K36me3, H3K79me2, H4K20me1 | 
| **В каких частях генома расположены** | CpG, экзоны, TSS,TSS2kb(начало транскрипции) | примерно равное распределение по всем категориям | ядерная ламина, TES(конец транскрипции) | экзоны, гены, TES, TSS2kb | Гены | Экзоны, гены, конец транскрипции, ядерная ламина | Ядерная ламина| Ядерная ламина, экзоныб конец транскрипции | Ядерная ламина (экзоны, гены, TES) | экзоны, гены, TES |
| **Расположение относительно старта транскрипции** | На TSS и по обе стороны | На TSS (до TSS) | (до TSS) | (До) и после TSS | - | - | - | На TSS (до TSS) | - | (До и после TSS) |
| **Расположение относительно конца транскрипции** | До, (на и после TES) | (До, на и после TES) | (после TES) | До, на (и после TES) | (До и на TES) | (До, на и после TES) | - | (До, на и после TES) | (До, на и после TES) | (До, на и после TES) | (До, на и после TES) |
| **Вывод** | Active Promoter | Enhancer 2 | Enhancer 1 | Weak promoter | Transcribed region 2 | Transcribed region 1 | Heterochromatin 1 | Heterochromatin 2 | Polycomb-repressed | Transcribed region 1/Enhancer | 

### Скриншоты бонусной части

![image](https://github.com/shaggy99999/hse_hw3_chromhmm/blob/main/images/2022-03-25_16-19-07.png)

![image](https://github.com/shaggy99999/hse_hw3_chromhmm/blob/main/images/2022-03-25_16-19-39.png)

Заменила номера состояний на соответствующие им названия

| **Номер состояния** | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 
| ------------- | ------------- |--------------------| -- | -- | -- | -- | -- | -- | -- | -- |
| **Название состояния** | act_prom | ench_2 | ench_1 | weak_prom | transc_reg_2 | transc_reg_1 | het_1 | het_2 | Pol_rep | tranreg_or_ench | 
