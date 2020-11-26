---
uid: Microsoft.Quantum.Synthesis.DecomposedOn
title: Функция Декомпоседон
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecomposedOn
qsharp.summary: Decomposes a permutation on a variable
ms.openlocfilehash: 79f952e7bc7ba9f5337cf5e7a625e0d270a2e17a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203235"
---
# <a name="decomposedon-function"></a>Функция Декомпоседон

Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

