---
uid: Microsoft.Quantum.Math.IsCoprimeL
title: Функция Ископримел
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: IsCoprimeL
qsharp.summary: Returns true if $a$ and $b$ are co-prime and false otherwise.
ms.openlocfilehash: c78e995801f67822cf98104a7319093d853b6afe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228140"
---
# <a name="iscoprimel-function"></a>Функция Ископримел

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает значение true, если $a $ и $b $ являются сопростыми, и false в противном случае.

```qsharp
function IsCoprimeL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a>Входные данные

### <a name="a--bigint"></a>a: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Первое число, для которого проверяется сопрималити


### <a name="b--bigint"></a>б: [bigint](xref:microsoft.quantum.lang-ref.bigint)

второе число, на которое проверяется сопрималити



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

True, если $a $ и $b $ являются совместно используемыми (например, их наибольший общий делитель равен 1), и false в противном случае