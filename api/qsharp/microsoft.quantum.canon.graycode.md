---
uid: Microsoft.Quantum.Canon.GrayCode
title: Функция Грайкоде
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: GrayCode
qsharp.summary: Creates Gray code sequences
ms.openlocfilehash: fc673ae21a952788b5beb74c1bad94ee9fe54480
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716167"
---
# <a name="graycode-function"></a>Функция Грайкоде

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Создает серые последовательности кода

```qsharp
function GrayCode (n : Int) : (Int, Int)[]
```


## <a name="input"></a>Входные данные

### <a name="n--int"></a>n: [int](xref:microsoft.quantum.lang-ref.int)

Число битов



## <a name="output--intint"></a>Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []

Массив кортежей. Первое значение кортежа является значением во втором значении последовательности Грайкоде в кортеже, которое изменяется в текущем значении для получения следующего.