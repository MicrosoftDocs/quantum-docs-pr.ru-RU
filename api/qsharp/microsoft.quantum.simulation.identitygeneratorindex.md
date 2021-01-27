---
uid: Microsoft.Quantum.Simulation.IdentityGeneratorIndex
title: Функция Идентитиженераториндекс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdentityGeneratorIndex
qsharp.summary: Returns a generator index consistent with the zero Hamiltonian, `H = 0`, which corresponds to the identity evolution operation.
ms.openlocfilehash: b389ca1e0737463e6ccd5ce885b849c6b32d65d1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844341"
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