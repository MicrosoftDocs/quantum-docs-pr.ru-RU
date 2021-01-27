---
uid: Microsoft.Quantum.Canon.TrotterStepSize
title: Функция Троттерстепсизе
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterStepSize
qsharp.summary: Computes Trotter step size in recursive implementation of Trotter simulation algorithm.
ms.openlocfilehash: c7b6432645dcad2bd47c62b91e04e0b42cd04ca9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840070"
---
# <a name="trotterstepsize-function"></a>Функция Троттерстепсизе

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Вычисление размера шага Троттер в рекурсивной реализации алгоритма моделирования Троттер.

```qsharp
function TrotterStepSize (order : Int) : Double
```


## <a name="input"></a>Входные данные

### <a name="order--int"></a>порядок: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--double"></a>Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>Remarks

В этой операции используется другое соглашение об индексировании, чем в [Куант-pH/0508139](https://arxiv.org/abs/quant-ph/0508139). В частности, `DecomposedIntoTimeStepsCA(_, 4)` соответствует скалярному $p _2 (\ламбда) $ в Куант-pH/0508139.