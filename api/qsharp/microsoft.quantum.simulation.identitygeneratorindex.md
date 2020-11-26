---
uid: Microsoft.Quantum.Simulation.IdentityGeneratorIndex
title: Функция Идентитиженераториндекс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdentityGeneratorIndex
qsharp.summary: Returns a generator index consistent with the zero Hamiltonian, `H = 0`, which corresponds to the identity evolution operation.
ms.openlocfilehash: 2dd3c705b0496df1719dc677e4defea5e435b839
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229296"
---
# <a name="identitygeneratorindex-function"></a>Функция Идентитиженераториндекс

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает индекс генератора, совместимый с нулевым Хамилтониан, `H = 0` который соответствует операции эволюции идентификаторов.

```qsharp
function IdentityGeneratorIndex (idxTerm : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a>Входные данные

### <a name="idxterm--int"></a>Идкстерм: [int](xref:microsoft.quantum.lang-ref.int)

Эти входные данные игнорируются и определяются для согласованности с <xref:microsoft.quantum.simulation.generatorsystem> определяемым пользователем типом.



## <a name="output--generatorindex"></a>Выходные данные: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Индекс генератора, представляющий развитие в Хамилтониан $H = $0.