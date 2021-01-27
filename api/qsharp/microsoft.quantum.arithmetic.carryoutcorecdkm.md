---
uid: Microsoft.Quantum.Arithmetic.CarryOutCoreCDKM
title: Операция Каррйоуткорекдкм
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CarryOutCoreCDKM
qsharp.summary: The core operation in the RippleCarryAdderCDKM, used with the above ApplyOuterCDKMAdder operation, i.e. conjugated with this operation to obtain the inner operation of the RippleCarryAdderCDKM. This operation computes the carry out qubit and applies a sequence of NOT gates on part of the input `ys`.
ms.openlocfilehash: 2065c767b341241d32e5ac06bcff0071cbadb266
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843345"
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