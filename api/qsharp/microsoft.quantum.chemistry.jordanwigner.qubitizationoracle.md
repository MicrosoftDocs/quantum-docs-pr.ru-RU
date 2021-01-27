---
uid: Microsoft.Quantum.Chemistry.JordanWigner.QubitizationOracle
title: Функция Кубитизатионоракле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: QubitizationOracle
qsharp.summary: Returns Qubitization operation and the parameters necessary to run it.
ms.openlocfilehash: cf6fe04b3f629c4ca4a7c27d8519a4cb42d07630
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835837"
---
# <a name="qubitizationoracle-function"></a>Функция Кубитизатионоракле

Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Возвращает операцию Кубитизатион и параметры, необходимые для ее запуска.

```qsharp
function QubitizationOracle (qSharpData : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData) : (Int, (Double, (Qubit[] => Unit is Adj + Ctl)))
```


## <a name="input"></a>Входные данные

### <a name="qsharpdata--jordanwignerencodingdata"></a>Кшарпдата: [жорданвигнеренкодингдата](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)

Хамилтониан, описанный в разделе `JordanWignerEncodingData` format.



## <a name="output--intdoublequbit--unit--is-adj--ctl"></a>Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int), ([Double](xref:microsoft.quantum.lang-ref.double),[кубит](xref:microsoft.quantum.lang-ref.qubit)[] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"))

Кортеж, где: `Int` — число Кубитс, `Double` — это одноразовая норма хамилтониан коэффициентов, а операция — это проход такта, созданный кубитизатион.