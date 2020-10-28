---
uid: Microsoft.Quantum.Math.ExtendedGreatestCommonDivisorI
title: Функция Екстендедгреатесткоммондивисори
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExtendedGreatestCommonDivisorI
qsharp.summary: Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: 8cb21ae5052ae6c5a8aed8be71d6bd3d32034272
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733057"
---
# <a name="extendedgreatestcommondivisori-function"></a>Функция Екстендедгреатесткоммондивисори

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакеты [](https://nuget.org/packages/)


Выполняет вычисление кортежа $ (u, v) $ таким, что $u \кдот a + v \кдот b = \Операторнаме{ГКД} (a, b) $, где $ \Операторнаме{ГКД} $ — $a $ наибольший общий делитель $a $ и $b $. GCD всегда имеет положительное значение.

```qsharp
function ExtendedGreatestCommonDivisorI (a : Int, b : Int) : (Int, Int)
```


## <a name="input"></a>Входные данные

### <a name="a--int"></a>ответ. [int](xref:microsoft.quantum.lang-ref.int)

Первое число, для которого вычисляются расширенные наибольшие общие делительы


### <a name="b--int"></a>б: [int](xref:microsoft.quantum.lang-ref.int)

второе число, для которого вычисляются расширенные наибольшие общие делительы



## <a name="output--intint"></a>Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))

Кортеж $ (u, v) $ со свойством $u \кдот + v \кдот b = \Операторнаме{ГКД} (a, b) $.

## <a name="references"></a>Ссылки

- Эта реализация в соответствии с https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm