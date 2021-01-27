---
uid: Microsoft.Quantum.Canon.ComposedOutput
title: Функция Компоседаутпут
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ComposedOutput
qsharp.summary: Returns the output of the composition of `inner` and `outer` for a given input.
ms.openlocfilehash: d39fcd6b2987b3a4f69df13fa83b69a199d6eddb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840888"
---
# <a name="composedoutput-function"></a>Функция Компоседаутпут

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

