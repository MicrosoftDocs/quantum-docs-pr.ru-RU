---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.ExpandedCoefficients
title: Функция ЕкспандедкоеффиЦиентс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: ExpandedCoefficients
qsharp.summary: Expands the compact representation of the Jordan-Wigner coefficients in order to obtain a one-to-one mapping between these and Pauli terms.
ms.openlocfilehash: b953fb8f5737956e8597cd90a7d6bfc0bafce4e3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835619"
---
# <a name="expandedcoefficients-function"></a>Функция ЕкспандедкоеффиЦиентс

Пространство имен: [Microsoft. тактов. химия. жорданвигнер. вке](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


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