---
uid: Microsoft.Quantum.Synthesis.FastHadamardTransformed
title: Функция Фассадамардтрансформед
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: FastHadamardTransformed
qsharp.summary: Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method
ms.openlocfilehash: be54413ef2d3fdaf7ddc726bc0906adb4ec382ff
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855449"
---
# <a name="fasthadamardtransformed-function"></a>Функция Фассадамардтрансформед

Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Вычисление Хадамард преобразования логической функции в {-1,1} кодировке с помощью метода Йейтса

```qsharp
function FastHadamardTransformed (func : Int[]) : Int[]
```


## <a name="input"></a>Входные данные

### <a name="func--int"></a>Func: [int](xref:microsoft.quantum.lang-ref.int)[]

Истинная таблица в {-1,1} кодировке



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]

Спектрал коэффициенты функции

## <a name="example"></a>Пример

```qsharp
FastHadamardTransformed([1, 1, 1, -1]); // [2, 2, 2, -2]
```