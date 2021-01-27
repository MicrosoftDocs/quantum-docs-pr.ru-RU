---
uid: Microsoft.Quantum.Canon.DecomposeIntoTimeStepsCA
title: Функция Декомпосеинтотиместепска
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DecomposeIntoTimeStepsCA
qsharp.summary: >-
  > [!WARNING]

  > DecomposeIntoTimeStepsCA has been deprecated. Please use <xref:Microsoft.Quantum.Canon.DecomposedIntoTimeStepsCA> instead.
ms.openlocfilehash: aa004098cbc805126109d3356f0f6550b85cd60b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840719"
---
# <a name="decomposeintotimestepsca-function"></a>Функция Декомпосеинтотиместепска

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> Декомпосеинтотиместепска является устаревшим. Взамен рекомендуется использовать <xref:Microsoft.Quantum.Canon.DecomposedIntoTimeStepsCA>.



```qsharp
function DecomposeIntoTimeStepsCA<'T> ((nSteps : Int, op : ((Int, Double, 'T) => Unit is Adj + Ctl)), trotterOrder : Int) : ((Double, 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="nsteps--int"></a>Нстепс: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="op--intdoublet--unit--is-adj--ctl"></a>Op: ([int](xref:microsoft.quantum.lang-ref.int),[Double](xref:microsoft.quantum.lang-ref.double), t) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"




### <a name="trotterorder--int"></a>Троттерордер: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--doublet--unit--is-adj--ctl"></a>Выходные данные: ([Double](xref:microsoft.quantum.lang-ref.double), t) => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

