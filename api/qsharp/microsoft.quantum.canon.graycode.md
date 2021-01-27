---
uid: Microsoft.Quantum.Canon.GrayCode
title: Функция Грайкоде
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: GrayCode
qsharp.summary: Creates Gray code sequences
ms.openlocfilehash: 0a9a19685f0511c44942df7d0bc8d257ad6b18c6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840501"
---
# <a name="graycode-function"></a>Функция Грайкоде

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Создает серые последовательности кода

```qsharp
function GrayCode (n : Int) : (Int, Int)[]
```


## <a name="input"></a>Входные данные

### <a name="n--int"></a>n: [int](xref:microsoft.quantum.lang-ref.int)

Число битов



## <a name="output--intint"></a>Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []

Массив кортежей. Первое значение кортежа является значением во втором значении последовательности Грайкоде в кортеже, которое изменяется в текущем значении для получения следующего.

## <a name="example"></a>Пример

```qsharp
GrayCode(2); // [(0, 0),(1, 1),(3, 0),(2, 1)]
```