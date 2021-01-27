---
uid: Microsoft.Quantum.Arithmetic.LittleEndian
title: Определяемый пользователем тип Литтлиндиан
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: LittleEndian
qsharp.summary: Register that encodes an unsigned integer in little-endian order. The qubit with index `0` encodes the lowest bit of an unsigned integer.
ms.openlocfilehash: 12bc4dbf830e426365545826575d66a9683cb694
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846566"
---
# <a name="littleendian-user-defined-type"></a>Определяемый пользователем тип Литтлиндиан

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Регистр кодирует целое число без знака в порядке с прямым порядком байтов. Кубит с индексом `0` кодирует наименьший бит целого числа без знака.

```qsharp

newtype LittleEndian = (Qubit[]);
```



## <a name="remarks"></a>Remarks

Мы предлагаем сокращение, `LittleEndian` как `LE` в документации.