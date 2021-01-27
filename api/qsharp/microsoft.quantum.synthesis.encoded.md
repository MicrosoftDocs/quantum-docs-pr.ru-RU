---
uid: Microsoft.Quantum.Synthesis.Encoded
title: Encoded, функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Encoded
qsharp.summary: Encode truth table in {1,-1} coding
ms.openlocfilehash: 44f6b247e6bfab7b55c46146cb63f8b6d219955b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855494"
---
# <a name="encoded-function"></a>Encoded, функция

Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Кодирование таблицы истинности в {1,-1} коде

```qsharp
function Encoded (table : Bool[]) : Int[]
```


## <a name="input"></a>Входные данные

### <a name="table--bool"></a>Таблица: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Истинная таблица как массив значений истинности



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]

Истинная таблица в виде массива {1,-1} целых чисел

## <a name="example"></a>Пример

```qsharp
Encoded([false, false, false, true]); // [1, 1, 1, -1]
```