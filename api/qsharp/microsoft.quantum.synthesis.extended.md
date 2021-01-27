---
uid: Microsoft.Quantum.Synthesis.Extended
title: Расширенная функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: Extended
qsharp.summary: Extends a spectrum by inverted coefficients
ms.openlocfilehash: 1855f3cab98c5fbf08c4505b90423df50cbec95b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855476"
---
# <a name="extended-function"></a>Расширенная функция

Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Расширяет спектр по инвертированным коэффициентам

```qsharp
function Extended (spectrum : Int[]) : Int[]
```


## <a name="input"></a>Входные данные

### <a name="spectrum--int"></a>спектр: [int](xref:microsoft.quantum.lang-ref.int)[]

Коэффициенты Спектрал



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)[]

Коэффициенты, за которыми следует инвертированная копия

## <a name="example"></a>Пример

```qsharp
Extended([2, 2, 2, -2]); // [2, 2, 2, -2, -2, -2, -2, 2]
```