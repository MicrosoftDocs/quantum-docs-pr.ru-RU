---
uid: Microsoft.Quantum.Arithmetic.BigEndian
title: Определяемый пользователем тип байтов
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: BigEndian
qsharp.summary: Register that encodes an unsigned integer in big-endian order. The qubit with index `0` encodes the highest bit of an unsigned integer.
ms.openlocfilehash: 64590606f7c36e0598a9d29c5c6a7ba6d6451aa1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731673"
---
# <a name="bigendian-user-defined-type"></a>Определяемый пользователем тип байтов

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакеты [](https://nuget.org/packages/)


Регистрация, которая кодирует целое число без знака в порядке с обратным порядком байтов. Кубит с индексом `0` кодирует наибольший бит целого числа без знака.

```qsharp

newtype BigEndian = (Qubit[]);
```



## <a name="remarks"></a>Remarks

Мы предлагаем сокращение, `BigEndian` как `BE` в документации.