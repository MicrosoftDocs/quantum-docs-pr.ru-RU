---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.ExpandedCoefficients
title: Функция ЕкспандедкоеффиЦиентс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: ExpandedCoefficients
qsharp.summary: Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.
ms.openlocfilehash: 8f5a2319b5839d0d9e47972389330dc16dffcaf0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713717"
---
# <a name="expandedcoefficients-function"></a>Функция ЕкспандедкоеффиЦиентс

Пространство имен: [Microsoft. тактов. химия. жорданвигнер. вке](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Пакеты [](https://nuget.org/packages/)


Развертывает компактное представление Jordan-Wigner коэффициенты для получения однозначного сопоставления между этими и Паули терминами.

```qsharp
function ExpandedCoefficients (coeff : Double[], termType : Int) : Double[]
```


## <a name="input"></a>Входные данные

### <a name="coeff--double"></a>коефф: [Double](xref:microsoft.quantum.lang-ref.double)[]

Массив коэффициентов, считываемых из структуры данных Jordan-Wigner Хамилтониан.


### <a name="termtype--int"></a>Термтипе: [int](xref:microsoft.quantum.lang-ref.int)

Тип Jordan-Wigner термина.



## <a name="output--double"></a>Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)[]

Расширенные массивы коэффициентов, по одному на каждый Паули термин.