---
uid: Microsoft.Quantum.Arithmetic.MultiplyByModularInteger
title: Операция Мултиплибимодуларинтежер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyByModularInteger
qsharp.summary: Performs modular multiplication by an integer constant on a qubit register.
ms.openlocfilehash: 080414d208a2a0c114857db8e93efb4cd74a4d8d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222581"
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



## <a name="remarks"></a>Комментарии

- Схема канала и описание см. на рис. 7 на [стр. 8 из арксив: Куант-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=8)
- Эта операция соответствует U ₐ в [арксив: Куант-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)