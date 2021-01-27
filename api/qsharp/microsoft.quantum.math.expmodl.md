---
uid: Microsoft.Quantum.Math.ExpModL
title: Функция Експмодл
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModL
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 127f2e51e19c76f4f7973bf1ac2217d4fffd72f6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848369"
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



## <a name="remarks"></a>Remarks

Принимает время пропорционально числу битов в `power` , а не в `power` самой.