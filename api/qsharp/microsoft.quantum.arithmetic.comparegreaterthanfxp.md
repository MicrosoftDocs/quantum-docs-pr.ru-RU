---
uid: Microsoft.Quantum.Arithmetic.CompareGreaterThanFxP
title: Операция Компарегреатерсанфксп
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGreaterThanFxP
qsharp.summary: Compares two fixed-point numbers stored in quantum registers, and controls a flip on the result.
ms.openlocfilehash: f49c713c8a1e8a6451f2c54fa59a72f00bfbb4c4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843324"
---
# <a name="comparegreaterthanfxp-operation"></a>Операция Компарегреатерсанфксп

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Сравнивает два числа с фиксированной запятой, хранящихся в тактовых регистрах, и управляет отражением результата.

```qsharp
operation CompareGreaterThanFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="fp1--fixedpoint"></a>FP1: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Первое сравниваемое число с фиксированной запятой.


### <a name="fp2--fixedpoint"></a>Fp2: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Второе сравниваемое число с фиксированной запятой.


### <a name="result--qubit"></a>результат: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Результат сравнения. Будет отражено, если `fp1 > fp2` .



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Текущая реализация требует, чтобы два числа с фиксированной запятой имели одно и то же расположение точки и одно и то же число Кубитс.