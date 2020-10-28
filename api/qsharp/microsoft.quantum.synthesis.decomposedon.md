---
uid: Microsoft.Quantum.Synthesis.DecomposedOn
title: Функция Декомпоседон
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecomposedOn
qsharp.summary: Decomposes a permutation on a variable
ms.openlocfilehash: b033723a50fb85e77c9d4baec1f94231327e9b25
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733913"
---
# <a name="decomposedon-function"></a>Функция Декомпоседон

Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)

Пакеты [](https://nuget.org/packages/)


Разделяет перестановку на переменную

```qsharp
function DecomposedOn (perm : Int[], index : Int) : ((Int[], Int[]), Int[])
```


## <a name="description"></a>Описание

Учитывая перестановку $ \пи $ ( `perm` ) и индекс $i $ ( `index` ), этот метод возвращает три перестановки $ ((\ pi_l, \ pi_r), \пи ") $ таким, что изображения $ \ pi_l $ и $ \ pi_r $ не изменяют биты в своих элементах в индексах, отличных от $i $ и изображений $ \пи" $ не меняйте бит $i $ в своих элементах.

## <a name="input"></a>Входные данные

### <a name="perm--int"></a>разрешение: [int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="index--int"></a>Индекс: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--intintint"></a>Выходные данные: (([int](xref:microsoft.quantum.lang-ref.int)[],[int](xref:microsoft.quantum.lang-ref.int)[]),[int](xref:microsoft.quantum.lang-ref.int)[])

