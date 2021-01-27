---
uid: Microsoft.Quantum.Math.PNormalized
title: Функция Пнормализед
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNormalized
qsharp.summary: >-
  Normalizes a vector of `Double`s in the `L(p)` norm.

  That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.
ms.openlocfilehash: ea6a88d07d3b246f666b793f0b10ab6598ea4ff6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854846"
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