---
uid: Microsoft.Quantum.MachineLearning.InputEncoder
title: Функция Инпутенкодер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state.
ms.openlocfilehash: 019161c0ef6cdec6875518ab58c8159b0f142149
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211752"
---
# <a name="inputencoder-function"></a>Функция Инпутенкодер

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Учитывая набор коэффициентов и допустимости, возвращает операцию подготовки состояния, которая подготавливает каждый коэффициент в качестве соответствующей амплитуды вычислительного состояния.

```qsharp
function InputEncoder (coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a>Входные данные

### <a name="coefficients--double"></a>коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]

Коэффициенты для кодирования во входное состояние.



## <a name="output--stategenerator"></a>Выходные данные: [статеженератор](xref:Microsoft.Quantum.MachineLearning.StateGenerator)

Операция подготовки состояния, которая подготавливает заданные коэффициенты в качестве входного состояния для заданного регистра.