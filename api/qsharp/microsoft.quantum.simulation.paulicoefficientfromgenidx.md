---
uid: Microsoft.Quantum.Simulation.PauliCoefficientFromGenIdx
title: Функция ПауликоеффиЦиентфромженидкс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliCoefficientFromGenIdx
qsharp.summary: Extracts the coefficient of a Pauli term described by a `GeneratorIndex`.
ms.openlocfilehash: 59ddadabb5c77cdb0d2e3620a09433992e85f663
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225063"
---
# <a name="paulicoefficientfromgenidx-function"></a>Функция ПауликоеффиЦиентфромженидкс

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Извлекает коэффициент Паули термина, описываемого `GeneratorIndex` .

```qsharp
function PauliCoefficientFromGenIdx (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Double
```


## <a name="input"></a>Входные данные

### <a name="generatorindex--generatorindex"></a>Женераториндекс: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

`GeneratorIndex` тип, который кодирует термин Паули.



## <a name="output--double"></a>Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)

Коэффициент термина, описываемого `GeneratorIndex` .