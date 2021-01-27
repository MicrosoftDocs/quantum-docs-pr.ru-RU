---
uid: Microsoft.Quantum.Research.Chemistry.OptimizedTrotterStepOracle
title: Функция Оптимизедтроттерстепоракле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: OptimizedTrotterStepOracle
qsharp.summary: Returns optimized Trotter step operation and the parameters necessary to run it.
ms.openlocfilehash: 523a31564ae5f054fd60161f9981c43d3467f3d9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842286"
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