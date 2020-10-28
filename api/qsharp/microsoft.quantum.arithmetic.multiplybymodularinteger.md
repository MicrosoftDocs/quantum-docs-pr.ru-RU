---
uid: Microsoft.Quantum.Arithmetic.MultiplyByModularInteger
title: Операция Мултиплибимодуларинтежер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyByModularInteger
qsharp.summary: Performs modular multiplication by an integer constant on a qubit register.
ms.openlocfilehash: 6deced7862ab4cb74315219eaaab97380cdf0f92
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730632"
---
# <a name="multiplybymodularinteger-operation"></a>Операция Мултиплибимодуларинтежер

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакеты [](https://nuget.org/packages/)


Выполняет модульное умножение с помощью целочисленной константы в регистре кубит.

```qsharp
operation MultiplyByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a>Описание

Отметим `modulus` , что $N $ и `constMultiplier` $a $.
Затем эта операция реализует единую операцию, определенную следующей картой на основе вычислений: $ $ \бегин{алигн} \кет{и} \мапсто \кет{(a \кдот y) \операторнаме{мод} N} \енд{алигн} $ $ для всех $y $ между $0 $ и $N-$1.

## <a name="input"></a>Входные данные

### <a name="constmultiplier--int"></a>Констмултиплиер: [int](xref:microsoft.quantum.lang-ref.int)

Константа, на которую умножается множитель. Должно быть состоять в виде модуля.


### <a name="modulus--int"></a>модуль: [int](xref:microsoft.quantum.lang-ref.int)

Операция умножения выполняется по модулю `modulus` .


### <a name="multiplier--littleendian"></a>множитель: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Число, умноженное на константу.
Это массив из Кубитс кодирования целого числа в формате с прямым порядком байтов.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

- Схема канала и описание см. на рис. 7 на [стр. 8 из арксив: Куант-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=8)
- Эта операция соответствует U ₐ в [арксив: Куант-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)