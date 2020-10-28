---
uid: Microsoft.Quantum.ErrorCorrection.InjectPi4YRotation
title: Операция InjectPi4YRotation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: InjectPi4YRotation
qsharp.summary: Rotates a single qubit by π/4 about the Y-axis.
ms.openlocfilehash: 8558767050c317661dfb490143fa3c8f4ea009e2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712318"
---
# <a name="injectpi4yrotation-operation"></a>Операция InjectPi4YRotation

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакеты [](https://nuget.org/packages/)


Поворачивает один кубит в π/4 о оси Y.

```qsharp
operation InjectPi4YRotation (data : Qubit, magic : Qubit) : Unit
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



## <a name="remarks"></a>Remarks

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