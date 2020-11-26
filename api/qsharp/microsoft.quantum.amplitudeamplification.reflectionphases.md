---
uid: Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
title: Определяемый пользователем тип Рефлектионфасес
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ReflectionPhases
qsharp.summary: Phases for a sequence of partial reflections in amplitude amplification.
ms.openlocfilehash: 743ece778239c223573a3a8536ae8059cea09d5f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191352"
---
# <a name="reflectionphases-user-defined-type"></a>Определяемый пользователем тип Рефлектионфасес

Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Этапы последовательности частичных отражений в усилении амплитуды.

```qsharp

newtype ReflectionPhases = (AboutStart : Double[], AboutTarget : Double[]);
```



## <a name="named-items"></a>Именованные элементы

### <a name="aboutstart--double"></a>Абаутстарт: [Double](xref:microsoft.quantum.lang-ref.double)[]

Массив этапов для отражения состояния запуска.
### <a name="abouttarget--double"></a>Абауттаржет: [Double](xref:microsoft.quantum.lang-ref.double)[]

Массив этапов для отражения состояния целевого объекта.

## <a name="remarks"></a>Комментарии

Оба массива должны иметь одинаковую длину. Обратите внимание, что во многих случаях первый этап о начальном состоянии и последнем этапе о целевом состоянии представляет собой смену глобального этапа и может иметь значение $0 $.