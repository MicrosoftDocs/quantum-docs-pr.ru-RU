---
uid: Microsoft.Quantum.Math.PNorm
title: Функция Пнорм
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNorm
qsharp.summary: >-
  Returns the `L(p)` norm of a vector of `Double`s.

  That is, given an array $x$ of type `Double[]`, this returns the $p$-norm $\|x\|\_p= (\sum_{j}|x_j|^{p})^{1/p}$.
ms.openlocfilehash: 3fe029bd893fc4d11aaf351f7ea566256cac5a9e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194735"
---
# <a name="pnorm-function"></a>Функция Пнорм

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает `L(p)` норму вектора типа `Double` .

То есть при наличии массива, $x $ типа `Double[]` , возвращается $p $-норма $ \| x \| \_ p = (\ sum_ {j} | x_j | ^ {p}) ^ {1/p} $.

```qsharp
function PNorm (p : Double, array : Double[]) : Double
```


## <a name="input"></a>Входные данные

### <a name="p--double"></a>p: [Double](xref:microsoft.quantum.lang-ref.double)

Экспонента $p $ в $p $-норме.


### <a name="array--double"></a>массив: [Double](xref:microsoft.quantum.lang-ref.double)[]





## <a name="output--double"></a>Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)

$P $-норма $ \| x \| _p $.