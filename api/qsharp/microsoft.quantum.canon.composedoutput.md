---
uid: Microsoft.Quantum.Canon.ComposedOutput
title: Функция Компоседаутпут
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ComposedOutput
qsharp.summary: Returns the output of the composition of `inner` and `outer` for a given input.
ms.openlocfilehash: 4da66616692055a7d60abbf1fac6e6799806675d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716489"
---
# <a name="composedoutput-function"></a>Функция Компоседаутпут

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Возвращает выходные данные композиции `inner` и для заданных `outer` входных данных.

```qsharp
function ComposedOutput<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U), target : 'T) : 'V
```


## <a name="input"></a>Входные данные

### <a name="outer--u---v"></a>Внешний: ' U-> ' V




### <a name="inner--t---u"></a>внутренний: не> "U




### <a name="target--t"></a>Целевой объект: 'T





## <a name="output--v"></a>Выходные данные: ' V



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е


### <a name="u"></a>' U


### <a name="v"></a>"V

