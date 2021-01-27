---
uid: Microsoft.Quantum.Arithmetic.BigEndian
title: Определяемый пользователем тип байтов
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: BigEndian
qsharp.summary: Register that encodes an unsigned integer in big-endian order. The qubit with index `0` encodes the highest bit of an unsigned integer.
ms.openlocfilehash: 2f6ec9f83ac124ce9b06c278f8fda820c35c23aa
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843391"
---
# <a name="bigendian-user-defined-type"></a>Определяемый пользователем тип байтов

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Регистрация, которая кодирует целое число без знака в порядке с обратным порядком байтов. Кубит с индексом `0` кодирует наибольший бит целого числа без знака.

```qsharp

newtype BigEndian = (Qubit[]);
```



## <a name="remarks"></a>Remarks

Мы предлагаем сокращение, `BigEndian` как `BE` в документации.