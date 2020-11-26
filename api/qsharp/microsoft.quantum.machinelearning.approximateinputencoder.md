---
uid: Microsoft.Quantum.MachineLearning.ApproximateInputEncoder
title: Функция Аппроксиматеинпутенкодер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ApproximateInputEncoder
qsharp.summary: Given a set of coefficients and a tolerance, returns a state preparation operation that prepares each coefficient as the corresponding amplitude of a computational basis state, up to the given tolerance.
ms.openlocfilehash: 2e39318cfaf3321c33b08f742bb25a9276b7e660
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196605"
---
# <a name="approximateinputencoder-function"></a>Функция Аппроксиматеинпутенкодер

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Учитывая набор коэффициентов и допустимости, возвращает операцию подготовки состояния, которая подготавливает каждый коэффициент в качестве соответствующей амплитуды вычислительного состояния, вплоть до заданного допуска.

```qsharp
function ApproximateInputEncoder (tolerance : Double, coefficients : Double[]) : Microsoft.Quantum.MachineLearning.StateGenerator
```


## <a name="input"></a>Входные данные

### <a name="tolerance--double"></a>Допуск: [Double](xref:microsoft.quantum.lang-ref.double)

Отклонение аппроксимации, используемое для кодирования заданных коэффициентов в входное состояние.


### <a name="coefficients--double"></a>коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]

Коэффициенты для кодирования во входное состояние.



## <a name="output--stategenerator"></a>Выходные данные: [статеженератор](xref:Microsoft.Quantum.MachineLearning.StateGenerator)

Операция подготовки состояния, которая подготавливает заданные коэффициенты в качестве входного состояния для заданного регистра.