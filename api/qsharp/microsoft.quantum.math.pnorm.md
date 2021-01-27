---
uid: Microsoft.Quantum.Math.PNorm
title: Функция Пнорм
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNorm
qsharp.summary: >-
  Returns the `L(p)` norm of a vector of `Double`s.

  That is, given an array $x$ of type `Double[]`, this returns the $p$-norm $\|x\|\_p= (\sum_{j}|x_j|^{p})^{1/p}$.
ms.openlocfilehash: 6207cca6cda5f9030facd31c327e58bdb9ecbf14
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847650"
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