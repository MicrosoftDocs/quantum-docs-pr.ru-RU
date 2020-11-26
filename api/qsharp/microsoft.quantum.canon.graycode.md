---
uid: Microsoft.Quantum.Canon.GrayCode
title: Функция Грайкоде
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: GrayCode
qsharp.summary: Creates Gray code sequences
ms.openlocfilehash: b15586c57180b00064721afc990436320824cba2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206890"
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