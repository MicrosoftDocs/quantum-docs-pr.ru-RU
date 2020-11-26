---
uid: Microsoft.Quantum.Math.ExpModI
title: Функция Експмоди
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModI
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 197f7351ce76ebb7684ca8014cab9ab65d9c784c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228497"
---
# <a name="expmodi-function"></a>Функция Експмоди

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает целое число, возведенное в заданную степень, по отношению к заданному модулю.

```qsharp
function ExpModI (expBase : Int, power : Int, modulus : Int) : Int
```


## <a name="description"></a>Описание

Давайте $x Експбасе $, Power by $p $ и модулем по $N $.
Функция возвращает $x ^ p \операторнаме{мод} N $.

Предполагается, что $N $, $x $ являются положительными, а энергопотребление не отрицательно.

## <a name="input"></a>Входные данные

### <a name="expbase--int"></a>Експбасе: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="power--int"></a>степень: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="modulus--int"></a>модуль: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)



## <a name="remarks"></a>Комментарии

Принимает время пропорционально числу битов в `power` , а не в `power` самой.