---
uid: Microsoft.Quantum.Arithmetic.BigEndian
title: Определяемый пользователем тип байтов
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: BigEndian
qsharp.summary: Register that encodes an unsigned integer in big-endian order. The qubit with index `0` encodes the highest bit of an unsigned integer.
ms.openlocfilehash: 8ea1aefa46a7224ef199baf68f2d6ab2d563e3a2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223669"
---
# <a name="bigendian-user-defined-type"></a>Определяемый пользователем тип байтов

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Регистрация, которая кодирует целое число без знака в порядке с обратным порядком байтов. Кубит с индексом `0` кодирует наибольший бит целого числа без знака.

```qsharp

newtype BigEndian = (Qubit[]);
```



## <a name="remarks"></a>Комментарии

Мы предлагаем сокращение, `BigEndian` как `BE` в документации.