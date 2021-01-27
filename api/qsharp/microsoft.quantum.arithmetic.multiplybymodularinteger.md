---
uid: Microsoft.Quantum.Arithmetic.MultiplyByModularInteger
title: Операция Мултиплибимодуларинтежер
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyByModularInteger
qsharp.summary: Performs modular multiplication by an integer constant on a qubit register.
ms.openlocfilehash: bd4e0ad6c5bad779d9a31139690021fd9fcda210
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846491"
---
# <a name="multiplybymodularinteger-operation"></a>Операция Мултиплибимодуларинтежер

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Выполняет модульное умножение с помощью целочисленной константы в регистре кубит.

```qsharp
operation MultiplyByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
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