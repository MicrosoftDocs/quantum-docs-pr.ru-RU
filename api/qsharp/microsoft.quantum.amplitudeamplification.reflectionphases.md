---
uid: Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
title: Определяемый пользователем тип Рефлектионфасес
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ReflectionPhases
qsharp.summary: Phases for a sequence of partial reflections in amplitude amplification.
ms.openlocfilehash: e0c7db6cd1aad636a34684958be117de1b9888f8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731969"
---
# <a name="reflectionphases-user-defined-type"></a>Определяемый пользователем тип Рефлектионфасес

Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)

Пакеты [](https://nuget.org/packages/)


Этапы последовательности частичных отражений в усилении амплитуды.

```qsharp

newtype ReflectionPhases = (AboutStart : Double[], AboutTarget : Double[]);
```



## <a name="named-items"></a>Именованные элементы

### <a name="aboutstart--double"></a>Абаутстарт: [Double](xref:microsoft.quantum.lang-ref.double)[]

Массив этапов для отражения состояния запуска.
### <a name="abouttarget--double"></a>Абауттаржет: [Double](xref:microsoft.quantum.lang-ref.double)[]

Массив этапов для отражения состояния целевого объекта.

## <a name="remarks"></a>Remarks

Оба массива должны иметь одинаковую длину. Обратите внимание, что во многих случаях первый этап о начальном состоянии и последнем этапе о целевом состоянии представляет собой смену глобального этапа и может иметь значение $0 $.