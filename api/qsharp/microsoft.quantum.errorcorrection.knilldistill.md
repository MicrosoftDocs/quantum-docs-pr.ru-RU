---
uid: Microsoft.Quantum.ErrorCorrection.KnillDistill
title: Операция Книллдистилл
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: KnillDistill
qsharp.summary: Implements the Knill magic state distillation algorithm.
ms.openlocfilehash: 1135db83cf750918347df10c6f1301b636aaee0c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712276"
---
# <a name="knilldistill-operation"></a>Операция Книллдистилл

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакеты [](https://nuget.org/packages/)


Реализует алгоритм Книлл "волшебного" состояния Magic.

```qsharp
operation KnillDistill (roughMagic : Qubit[]) : Bool
```


## <a name="description"></a>Описание

Учитывая 15 приблизительных копий волшебного состояния $ $ \бегин{алигн} \кос\фрак{\пи} {8} \кет {0} + \син \фрак{\пи} {8} \кет {1} \енд{алигн}, $ $ дает одну копию более высокого качества.

## <a name="input"></a>Входные данные

### <a name="roughmagic--qubit"></a>Раугхмагик: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр пятнадцать Кубитс, содержащий приблизительные копии волшебного состояния. После применения этой процедуры `roughMagic[0]` перенастройки будет содержаться одна копия высокого качества, а оставшаяся часть регистра вернется к состоянию $ \ket{00\cdots 0} $.



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

Если `true` значение равно, то процедура прошла удачно и будет принята копия более высокого качества. Если `false` значение равно, то процедура завершилась ошибкой, а состояние регистра должно считаться неопределенным.

## <a name="remarks"></a>Remarks

Мы будем следовать алгоритму Книлл.
Однако представленная реализация далеко не является оптимальной, так как она использует слишком много Кубитс.
В этой подпрограммы добавлены волшебные состояния, в которых есть более эффективные протоколы.

## <a name="references"></a>Ссылки

- [книлл](https://arxiv.org/abs/quant-ph/0402171)