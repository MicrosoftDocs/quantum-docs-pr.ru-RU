---
uid: Microsoft.Quantum.Math.BitSizeL
title: Функция Битсизел
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeL
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: 8b3d4cceb69619ed32977337fc0fe7401db38cbd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211055"
---
# <a name="bitsizel-function"></a>Функция Битсизел

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Для неотрицательного целого числа `a` возвращает число битов, необходимых для представления `a` .

То есть возвращает наименьшее $n $ например, $a < 2 ^ n $.

```qsharp
function BitSizeL (a : BigInt) : Int
```


## <a name="input"></a>Входные данные

### <a name="a--bigint"></a>a: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Целое число, для которого требуется вычислить битовую длину.



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Разрядный размер `a` .