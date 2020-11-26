---
uid: Microsoft.Quantum.Research.Chemistry.OptimizedTrotterStepOracle
title: Функция Оптимизедтроттерстепоракле
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: OptimizedTrotterStepOracle
qsharp.summary: Returns optimized Trotter step operation and the parameters necessary to run it.
ms.openlocfilehash: 04b1ea457277e0681596cb564fae3782a2d09db9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229823"
---
# <a name="optimizedtrottersteporacle-function"></a>Функция Оптимизедтроттерстепоракле

Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)

Пакет: [Microsoft. тактов. Research. Химия](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)


Возвращает оптимизированную операцию Троттер шага и параметры, необходимые для ее запуска.

```qsharp
function OptimizedTrotterStepOracle (qSharpData : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, trotterStepSize : Double, trotterOrder : Int) : (Int, (Double, (Qubit[] => Unit is Adj + Ctl)))
```


## <a name="input"></a>Входные данные

### <a name="qsharpdata--jordanwignerencodingdata"></a>Кшарпдата: [жорданвигнеренкодингдата](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)

Хамилтониан, описанный в разделе `JordanWignerEncodingData` format.


### <a name="trotterstepsize--double"></a>Троттерстепсизе: [Double](xref:microsoft.quantum.lang-ref.double)

Размер шага Троттер Integrator.


### <a name="trotterorder--int"></a>Троттерордер: [int](xref:microsoft.quantum.lang-ref.int)

Порядок Троттер интегратора.



## <a name="output--intdoublequbit--unit--is-adj--ctl"></a>Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int), ([Double](xref:microsoft.quantum.lang-ref.double),[кубит](xref:microsoft.quantum.lang-ref.qubit)[] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"))

Кортеж, где: `Int` — число Кубитс, `Double` равно `1.0/trotterStepSize` , а операция — шаг Троттер.