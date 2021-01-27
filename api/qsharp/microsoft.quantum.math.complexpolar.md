---
uid: Microsoft.Quantum.Math.ComplexPolar
title: Определяемый пользователем тип Комплексполар
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ComplexPolar
qsharp.summary: >-
  Represents a complex number in polar form.

  The polar representation of a complex number is $c=r e^{i t}$.
ms.openlocfilehash: 174e75b82a3ee740cd4d07e5bcd091de65bbc6b6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847352"
---
# <a name="complexpolar-user-defined-type"></a>Определяемый пользователем тип Комплексполар

Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Представляет комплексное число в полярной форме.

Полярное представление комплексного числа имеет $c = r e ^ {i t} $.

```qsharp

newtype ComplexPolar = (Magnitude : Double, Argument : Double);
```



## <a name="named-items"></a>Именованные элементы

### <a name="magnitude--double"></a>Величина: [Double](xref:microsoft.quantum.lang-ref.double)

Абсолютное значение $r \же $0 из $c $.
### <a name="argument--double"></a>Аргумент: [Double](xref:microsoft.quantum.lang-ref.double)

Фаза $t \ин \масбб R $ of $c $.