---
uid: Microsoft.Quantum.Math.IsCoprimeL
title: Функция Ископримел
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: IsCoprimeL
qsharp.summary: Returns true if $a$ and $b$ are co-prime and false otherwise.
ms.openlocfilehash: a48f056d138499607d32b38b1fa0970745732c41
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851343"
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