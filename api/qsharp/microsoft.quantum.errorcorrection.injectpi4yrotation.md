---
uid: Microsoft.Quantum.ErrorCorrection.InjectPi4YRotation
title: Операция InjectPi4YRotation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: InjectPi4YRotation
qsharp.summary: Rotates a single qubit by π/4 about the Y-axis.
ms.openlocfilehash: 4ff0abe67a6d18204e417a45f8d8f1d092d02b88
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200804"
---
# <a name="injectpi4yrotation-operation"></a>Операция InjectPi4YRotation

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Поворачивает один кубит в π/4 о оси Y.

```qsharp
operation InjectPi4YRotation (data : Qubit, magic : Qubit) : Unit is Adj
```


## <a name="description"></a>Описание

Выполняет поворот π/4 о `Y` .

Поворот выполняется путем использования волшебного состояния; то есть копия State $ $ \бегин{алигн} \кос\фрак{\пи} {8} \кет {0} + \син \фрак{\пи} {8} \кет {1} .
\енд{алигн} $ $

## <a name="input"></a>Входные данные

### <a name="data--qubit"></a>данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Объект кубит, повернутый около $Y $ by $ \пи/$4.


### <a name="magic--qubit"></a>волшебность: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит изначально находится в состоянии Magic. После применения этой операции возвращается в `magic` состояние $ \кет {0} $.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Комментарии

Следующие эквивалентны:

```qsharp
Ry(PI() / 4.0, data);
```

и

```qsharp
using (magic = Qubit()) {
    Ry(PI() / 4.0, magic);
    InjectPi4YRotation(data, magic);
    Reset(magic);
}
```

Эта операция поддерживает `Adjoint` функтор, в этом случае используется одно и то же магическое состояние, но воздействие на кубит данных — это вращение $-\ PI/4 $ $Y $-.