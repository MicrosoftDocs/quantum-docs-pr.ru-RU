---
uid: Microsoft.Quantum.Canon.TrotterStepSize
title: Функция Троттерстепсизе
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterStepSize
qsharp.summary: Computes Trotter step size in recursive implementation of Trotter simulation algorithm.
ms.openlocfilehash: aa5b63e058e1ea726b0d4c6eca73078831daaf3b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204697"
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



## <a name="remarks"></a>Комментарии

В этой операции используется другое соглашение об индексировании, чем в [Куант-pH/0508139](https://arxiv.org/abs/quant-ph/0508139). В частности, `DecomposedIntoTimeStepsCA(_, 4)` соответствует скалярному $p _2 (\ламбда) $ в Куант-pH/0508139.