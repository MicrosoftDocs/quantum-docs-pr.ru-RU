---
uid: Microsoft.Quantum.Math.PNormalized
title: Функция Пнормализед
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNormalized
qsharp.summary: >-
  Normalizes a vector of `Double`s in the `L(p)` norm.

  That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.
ms.openlocfilehash: 196bdab67528aa8672a010ac3830459e27276ce9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227528"
---
# <a name="pnormalized-function"></a>Функция Пнормализед

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Нормализация вектора `Double` s в `L(p)` норме.

То есть при наличии массива, $x $ типа `Double[]` , возвращается массив, в котором все элементы делятся на $p $-норму $ \| x \| _p $.

```qsharp
function PNormalized (p : Double, array : Double[]) : Double[]
```


## <a name="input"></a>Входные данные

### <a name="p--double"></a>p: [Double](xref:microsoft.quantum.lang-ref.double)

Экспонента $p $ в $p $-норме.


### <a name="array--double"></a>массив: [Double](xref:microsoft.quantum.lang-ref.double)[]





## <a name="output--double"></a>Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)[]

Массив $x $ нормализован $p $-нормой $ \| x \| _p $.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Math. Пнорм](xref:Microsoft.Quantum.Math.PNorm)