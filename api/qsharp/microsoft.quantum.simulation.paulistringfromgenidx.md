---
uid: Microsoft.Quantum.Simulation.PauliStringFromGenIdx
title: Функция Паулистрингфромженидкс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliStringFromGenIdx
qsharp.summary: Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.
ms.openlocfilehash: a937dc648c5de5a5f6de7da996448af497b92185
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230316"
---
# <a name="paulistringfromgenidx-function"></a>Функция Паулистрингфромженидкс

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Извлекает строку Паули и ее индексы кубит для термина Паули, описанного в `GeneratorIndex` .

```qsharp
function PauliStringFromGenIdx (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : (Pauli[], Int[])
```


## <a name="input"></a>Входные данные

### <a name="generatorindex--generatorindex"></a>Женераториндекс: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

`GeneratorIndex` тип, который кодирует термин Паули.



## <a name="output--pauliint"></a>Выходные данные: ([Паули](xref:microsoft.quantum.lang-ref.pauli)[],[int](xref:microsoft.quantum.lang-ref.int)[])

Строка Паули термина, описываемая `GeneratorIndex` , и индексы для Кубитс, с которой он работает.