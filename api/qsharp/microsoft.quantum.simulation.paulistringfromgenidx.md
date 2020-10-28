---
uid: Microsoft.Quantum.Simulation.PauliStringFromGenIdx
title: Функция Паулистрингфромженидкс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliStringFromGenIdx
qsharp.summary: Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.
ms.openlocfilehash: 33da4bc3d7e58b87aef75b453b6af09a51214923
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710540"
---
# <a name="paulistringfromgenidx-function"></a>Функция Паулистрингфромженидкс

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакеты [](https://nuget.org/packages/)


Извлекает строку Паули и ее индексы кубит для термина Паули, описанного в `GeneratorIndex` .

```qsharp
function PauliStringFromGenIdx (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : (Pauli[], Int[])
```


## <a name="input"></a>Входные данные

### <a name="generatorindex--generatorindex"></a>Женераториндекс: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

`GeneratorIndex` тип, который кодирует термин Паули.



## <a name="output--pauliint"></a>Выходные данные: ([Паули](xref:microsoft.quantum.lang-ref.pauli)[],[int](xref:microsoft.quantum.lang-ref.int)[])

Строка Паули термина, описываемая `GeneratorIndex` , и индексы для Кубитс, с которой он работает.