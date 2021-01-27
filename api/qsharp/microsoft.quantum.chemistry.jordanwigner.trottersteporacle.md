---
uid: Microsoft.Quantum.Chemistry.JordanWigner.TrotterStepOracle
title: Функция Троттерстепоракле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: TrotterStepOracle
qsharp.summary: Returns Trotter step operation and the parameters necessary to run it.
ms.openlocfilehash: a3164da1ce9ae1f72ec2fb1fa151159768cd5a4a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835800"
---
# <a name="trottersteporacle-function"></a>Функция Троттерстепоракле

Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Возвращает операцию Троттер шага и параметры, необходимые для ее запуска.

```qsharp
function TrotterStepOracle (qSharpData : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, trotterStepSize : Double, trotterOrder : Int) : (Int, (Double, (Qubit[] => Unit is Adj + Ctl)))
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