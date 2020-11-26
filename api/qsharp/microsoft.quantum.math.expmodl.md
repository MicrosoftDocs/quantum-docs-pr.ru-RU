---
uid: Microsoft.Quantum.Math.ExpModL
title: Функция Експмодл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModL
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 07da113caeb9f6f3f3f3f92f13478f33021bfa14
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210757"
---
# <a name="expmodl-function"></a>Функция Експмодл

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает целое число, возведенное в заданную степень, по отношению к заданному модулю.

```qsharp
function ExpModL (expBase : BigInt, power : BigInt, modulus : BigInt) : BigInt
```


## <a name="description"></a>Описание

Давайте $x Експбасе $, Power by $p $ и модулем по $N $.
Функция возвращает $x ^ p \операторнаме{мод} N $.

Предполагается, что $N $, $x $ являются положительными, а энергопотребление не отрицательно.

## <a name="input"></a>Входные данные

### <a name="expbase--bigint"></a>Експбасе: [bigint](xref:microsoft.quantum.lang-ref.bigint)




### <a name="power--bigint"></a>степень: [bigint](xref:microsoft.quantum.lang-ref.bigint)




### <a name="modulus--bigint"></a>модуль: [bigint](xref:microsoft.quantum.lang-ref.bigint)





## <a name="output--bigint"></a>Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)



## <a name="remarks"></a>Комментарии

Принимает время пропорционально числу битов в `power` , а не в `power` самой.