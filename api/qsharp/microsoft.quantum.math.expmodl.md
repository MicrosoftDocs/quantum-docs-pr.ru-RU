---
uid: Microsoft.Quantum.Math.ExpModL
title: Функция Експмодл
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModL
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 73d434bd364847b4e5e06d1a9f460424e0c50850
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733064"
---
# <a name="expmodl-function"></a>Функция Експмодл

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакеты [](https://nuget.org/packages/)


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



## <a name="remarks"></a>Remarks

Принимает время пропорционально числу битов в `power` , а не в `power` самой.