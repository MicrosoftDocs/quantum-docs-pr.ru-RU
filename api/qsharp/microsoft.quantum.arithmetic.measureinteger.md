---
uid: Microsoft.Quantum.Arithmetic.MeasureInteger
title: Операция Меасуреинтежер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MeasureInteger
qsharp.summary: Measures the content of a quantum register and converts it to an integer. The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.
ms.openlocfilehash: e3ff06e5cbb2ef8a63e4ad12308b382347c90fc3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222649"
---
# <a name="measureinteger-operation"></a>Операция Меасуреинтежер

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Измеряет содержимое регистра такта и преобразует его в целое число. Измерение выполняется в соответствии со стандартной вычислительной единицей, т. е. еиженбасис `PauliZ` .

```qsharp
operation MeasureInteger (target : Microsoft.Quantum.Arithmetic.LittleEndian) : Int
```


## <a name="input"></a>Входные данные

### <a name="target--littleendian"></a>Целевой объект: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Регистр такта в кодировке с прямым порядком байтов.



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Целое число без знака, содержащее измеряемое значение `target` .

## <a name="remarks"></a>Комментарии

Эта операция сбрасывает регистр входных данных в состояние $ \ket{00\cdots 0} $, подходящее для освобождения на целевом компьютере.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Меасуреинтежербе](xref:Microsoft.Quantum.Canon.MeasureIntegerBE)