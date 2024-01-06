# CUDA PI calculation
Calculating the number of pi by the Monte Carlo method using CUDA technology<br>
In this work, 256 CUDA blocks from 265 to 256 threads in each were used. Each thread produces N experiments, writing down the local result in an array of common memory. After that, all results are added and divided by the number of flows, as a result, we get the overall result of the calculations.

Вычисление числа Пи методом Монте-Карло с использованием технологии CUDA <br>
В этой работе использовалось 256 блоков CUDA с 265 на 256 нитей в каждом. Каждая нить производит N экспериментов, записывая локальный результат в массив общей памяти. После чего все результаты складываются и делятся на число потоков, в итоге мы получаем общий результат вычислений.

## Экспериментальные результаты
Эксперименты производились с использованием процессора AMD Ryzen 5 2600 и графического ускорителя NVIDIA GeForce RTX 2060.
| N             | Время последовательного выполнения, ms  | Время паралелльного выполнения, ms  | Ускорение 
| :-----------: |:---------------------------------------:| :----------------------------------:| :-------: |
| 1             |    8                                    |   539                               |       0.01|
| 64            |    463                                  |   523                               |       0.88|
| 256           |    1879                                 |   543                               |       3.46|
| 1024          |    7552                                 |   538                               |      14.03|
| 2048          |    15228                                |   615                               |      24.76|

2020.