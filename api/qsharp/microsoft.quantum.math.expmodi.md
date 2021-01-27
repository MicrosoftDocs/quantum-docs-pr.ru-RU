---
uid: Microsoft.Quantum.Math.ExpModI
title: Функция Експмоди
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModI
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: dd4fc7d98275f6a02e3b13163b92f0812c92a82f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857035"
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



## <a name="remarks"></a>Remarks

Принимает время пропорционально числу битов в `power` , а не в `power` самой.