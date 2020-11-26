---
uid: Microsoft.Quantum.Arithmetic.CarryOutCoreCDKM
title: Операция Каррйоуткорекдкм
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CarryOutCoreCDKM
qsharp.summary: The core operation in the RippleCarryAdderCDKM, used with the above ApplyOuterCDKMAdder operation, i.e. conjugated with this operation to obtain the inner operation of the RippleCarryAdderCDKM. This operation computes the carry out qubit and applies a sequence of NOT gates on part of the input `ys`.
ms.openlocfilehash: 19a692a3b54a413f25a474c361e773ab6c65579e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223550"
---
# <a name="carryoutcorecdkm-operation"></a>Операция Каррйоуткорекдкм

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Основная операция в Рипплекарряддеркдкм, используемая с приведенной выше операцией Апплйоутеркдкмаддер, которая была сопряжена с этой операцией для получения внутренней операции Рипплекарряддеркдкм. Эта операция выполняет вычисление кубит и применяет последовательность нешлюзов для части входных данных `ys` .

```qsharp
operation CarryOutCoreCDKM (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, ancilla : Qubit, carry : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="xs--littleendian"></a>xs: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Первый кубит регистр.


### <a name="ys--littleendian"></a>ИС: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Второй кубит регистр.


### <a name="ancilla--qubit"></a>анЦилла: [кубит](xref:microsoft.quantum.lang-ref.qubit)

АнЦилла кубит, используемый в Рипплекарряддеркдкм, передан в эту операцию.


### <a name="carry--qubit"></a>выполнение: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Выполните кубит в операции Рипплекарряддеркдкм.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Ссылки

- Андрей A. Куккаро, Томас G. Драпер, Самуел A. Кутин, Дэвид Петрие Маултон: "Новая тактовая цепь Ripple — комплексное сложение", 2004.
  https://arxiv.org/abs/quant-ph/0410184v1