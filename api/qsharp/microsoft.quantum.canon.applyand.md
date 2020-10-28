---
uid: Microsoft.Quantum.Canon.ApplyAnd
title: Операция нажимаем
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyAnd
qsharp.summary: Inverts a given target qubit if and only if both control qubits are in the 1 state, using measurement to perform the adjoint operation.
ms.openlocfilehash: 5a4e18cb0361708e1fc00e8d62c0a6c2415d6bed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729744"
---
# <a name="applyand-operation"></a>Операция нажимаем

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Инвертирует заданный целевой объект кубит только в том случае, если оба элемента управления Кубитс находятся в состоянии 1, с помощью измерения для выполнения примыкающей операции.

```qsharp
operation ApplyAnd (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit
```


## <a name="description"></a>Описание

Инвертирует `target` , если оба элемента управления равны 1, но предполагает, что `target` находится в состоянии 0.  Операция имеет T-Count 4, T-Depth 2 и не требует вспомогательных кубит и, следовательно, может быть предпочтительней для операции ККНОТ, если `target` известно как 0.  Смежная операция основана на измерении и не требует T-шлюзов.

Для управляемого приложения этой операции не требуются вспомогательные кубит, `2^c` `Rz` шлюзы и не оптимизированы для глубины, где `c` — это число общего Кубитс управления, включая два элемента управления из `ApplyAnd` операции.  Для приложения, контролируемого соседним контролем `2^c - 1` `Rz` , требуются шлюзы (с углом, равным вдвое меньше размера несмежной операции), вспомогательный кубит не оптимизирован и не оптимизируется для глубины.

## <a name="input"></a>Входные данные

### <a name="control1--qubit"></a>Control1: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Первый элемент управления кубит


### <a name="control2--qubit"></a>control2: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Второй элемент управления кубит


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Целевой вспомогательный кубит; должно находиться в состоянии 0



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Ссылки

- Коди Jones: "романские конструкции для отказоустойчивого Тоффоли шлюза", инвентаризационная. Rev. A 87, 022328, 2013 [арксив: 1212.5069](https://arxiv.org/abs/1212.5069) ДОИ: 10.1103/фисрева. 87.022328
- Крейг Гиднэй: "сократить затраты на сложение тактов", такт 2, страница 74, 2018 [арксив: 1709.06648](https://arxiv.org/abs/1709.06648) ДОИ: 10.1103/фисрева. 85.044302
- Матиас Соекен: "каналы Oracle для тактов и шаблон дерева Рождества", [статья блога 19 декабря 2019](https://msoeken.github.io/blog_qac.html) (Примечание: объясняется многоуправляемая конструкция).