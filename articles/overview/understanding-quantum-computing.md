---
title: Общие сведения о квантовых вычислениях
description: Что такое квантовые компьютеры и как в них используются принципы квантовой механики?
author: bradben
ms.author: bradben
ms.date: 5/5/2020
ms.topic: overview
uid: microsoft.quantum.overview.understanding
ms.openlocfilehash: 65fa85a80021124444fd352f9492d03cbefcb859
ms.sourcegitcommit: a03d79ca3f0774161a9f86a15528d36e1291acce
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2020
ms.locfileid: "83433016"
---
# <a name="understanding-quantum-computing"></a>Общие сведения о квантовых вычислениях

В квантовых вычислениях для обработки информации используются принципы квантовой механики. По этой причине для них требуется иной подход, чем для традиционных вычислений.  Одним из примеров такого отличия является используемый в квантовых компьютерах процессор.  Обычные компьютеры используют знакомые нам кремниевые микросхемы, а квантовые компьютеры — такие квантовые материалы, как атомы, ионы, фотоны и электроны.  

Эти квантовые материалы ведут себя в соответствии с законами квантовой механики. Их поведение описывают такие понятия, как вероятностные вычисления, суперпозиция и запутанность. Эти понятия, в свою очередь, являются основой квантовых алгоритмов, которые позволяют использовать возможности квантовых вычислений для решения сложных задач. В этой статье описываются некоторые основные понятия квантовой механики, лежащие в основе квантовых вычислений.

## <a name="a-birds-eye-view-of-quantum-mechanics"></a>Общие сведения о квантовой механике

Квантовая механика (или квантовая теория) — это раздел физики, изучающий частицы на атомном и субатомном уровнях. При этом многие законы традиционной механики не применяются на квантовом уровне. В основе квантовых вычислений лежат три явления — суперпозиция, квантовое измерение и запутанность.  

### <a name="superposition-vs-binary-computing"></a>Суперпозиция и двоичные вычисления

Представьте, что вы тренируетесь у себя в комнате. Вы выполняете полный поворот налево, а затем полный поворот направо. Теперь попробуйте повернуться одновременно и налево, и направо. Вы не можете это сделать (по крайней мере таким образом, чтобы не разорваться на две части).  Очевидно, что вы не можете находиться в обоих этих состояниях одновременно, то есть вы не можете смотреть налево и направо одновременно.

Но если бы вы были квантовой частицей, то у вас была бы определенная вероятность *выполнить поворот налево* И определенная вероятность *выполнить поворот направо*. Это возможно благодаря явлению, которое называется **суперпозицией** (или **когерентностью**).

Квантовая частица, в частности электрон, имеет собственные свойства поворота налево или направо, например **спин**, ориентированный вверх или вниз, или, оперируя более традиционными понятиями бинарных вычислений, значение 1 или 0. Когда квантовая частица находится в состоянии суперпозиции, это линейная комбинация бесконечного числа состояний между 1 до 0. Но вы не знаете, в каком именно состоянии она находится, пока не посмотрите на нее. здесь мы переходим к следующему явлению — **квантовому измерению**.

### <a name="quantum-measurement"></a>Квантовое измерение

Теперь представим, что к вам пришел друг, который хочет сфотографировать вас во время тренировки. Скорее всего, он получит ваше размытое изображение во время поворота — где-то между крайней левой и правой точками.

Но если бы вы были квантовой частицей, произошло бы нечто интересное. Независимо от вашего реального положения, на снимке вы будете изображены так, будто выполнили полный левый или правый поворот.

Так происходит потому, что процесс наблюдения или измерения квантовой частицы приводит к **коллапсу** состояния суперпозиции (происходит **декогеренция**), и частица переходит в классическое бинарное состояние: 1 или 0.

Это бинарное состояние удобно для нас, так как компьютеры могут выполнять множество операций со значениями 1 и 0. При этом когда квантовая частица измеряется и коллапсирует, она навсегда (как и вы на фотографии) остается в этом состоянии, определяемым значением 1 или 0. Тем не менее, как вы увидите позже, в квантовых вычислениях существуют операции, которые могут вернуть частицу обратно в состояние суперпозиции, чтобы ее можно было снова использовать для квантовых вычислений.

### <a name="entanglement"></a>Запутанность

Возможно, наиболее интересным явлением квантовой механики является способность двух или более квантовых частиц **запутываться** друг с другом. Когда частицы запутываются, они образуют единую систему, и квантовое состояние любой из них не может быть описано независимо от квантового состояния других частиц. Это означает, что любая операция или процесс, который вы применяете к одной частице, влияет и на другие частицы.

Наряду с этой взаимозависимостью частицы могут поддерживать связь, даже будучи разделенными на невероятно большие расстояния (вплоть до таких, которые измеряются световыми годами). Эффекты квантового измерения также применимы к запутанным частицам, поэтому, когда одна частица измеряется и коллапсирует, другая тоже коллапсирует. Так как между запутанными кубитами существует корреляция, при измерении состояния одного кубита можно получить сведения о состоянии другого. Это свойство очень полезно в квантовых вычислениях.

### <a name="qubits-and-probability"></a>Кубиты и вероятность

Обычные компьютеры хранят и обрабатывают информацию в битах, которые могут иметь состояние, определяемое значением 1 или 0, но не обеими значениями одновременно. Эквивалентом этому в квантовых вычислениях является **кубит**, который представляет состояние квантовой частицы. Из-за суперпозиции кубиты могут иметь значение 1 либо 0 или промежуточное значение. В зависимости от конфигурации, кубит имеет определенную *вероятность* сколлапсировать до 1 или 0. Эта вероятность коллапса в одно или другое состояние определяется **квантовой интерференцией**. 

Помните друга, который вас фотографировал? Предположим, у него есть специальные фильтры на камере, называемые *интерференционными*. Если выбрать фильтр *70/30* и начать фотографировать, на 70 % снимков вы будете смотреть налево, а на 30 % — направо. Фильтр изменил обычное состояние камеры, чтобы повлиять на вероятность, определяющую ее поведение.

Аналогичным образом квантовая интерференция воздействует на состояние кубита, чтобы повлиять на вероятность получения определенного результата во время измерения. Этот вероятностный характер и делает квантовые вычисления такими мощными.

Например, мы можем взять два бита, лежащих в основе обычных вычислений. Каждый из них может принимать значение 1 или 0, следовательно, всего вы можете хранить четыре возможных значения: **00**, **01**, **10** и **11**. При этом в определенный момент времени доступно только одно такое значение. Но при наличии двух кубитов в суперпозиции каждый из них может иметь значение 1, 0 или *оба* эти значения, поэтому вы можете получить те же самые четыре значения одновременно. С тремя кубитами вы получаете восемь значений, с четырьмя кубитами — 16 значений и т. д.

## <a name="summary"></a>Сводка

Эти важные фундаментальные понятия описывают квантовую механику очень поверхностно. Но они лежат в основе квантовых вычислений.

- **Суперпозиция** — способность квантовых частиц представлять комбинацию всех возможных состояний.
- **Квантовое измерение** — процесс наблюдения за квантовыми частицами в суперпозиции, что приводит к переходу в одно из возможных состояний.
- **Запутанность** — взаимозависимость квантовых частиц, когда результаты измерения одних частиц влияют на состояние других.
- **Кубит** — базовая единица информации в квантовых вычислениях. Кубит — это квантовая частица, которая находится в суперпозиции всех возможных состояний.
- **Интерференция** — внутреннее поведение кубита, обусловленное суперпозицией, которое влияет на вероятность его коллапса в одно из состояний.

## <a name="next-steps"></a>Next Steps

> [!div class="nextstepaction"]
> [Квантовые компьютеры и квантовые симуляторы](xref:microsoft.quantum.overview.simulators)