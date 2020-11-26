---
uid: Microsoft.Quantum.Simulation.PauliBlockEncoding
title: Функция Паулиблоккенкодинг
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: b1df6d239e6ef061cf0a4784c652e9dd126991d5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230435"
---
# <a name="pauliblockencoding-function"></a>Функция Паулиблоккенкодинг

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Создает единое блочное кодирование для Хамилтониан.

Хамилтониан $H = \ sum_ {j} \ alpha_j P_j $ описывается суммой Паулиных терминов $P _j $, каждый с действительным коэффициентом $ \ alpha_j $.

```qsharp
function PauliBlockEncoding (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Double, Microsoft.Quantum.Simulation.BlockEncodingReflection)
```


## <a name="input"></a>Входные данные

### <a name="generatorsystem--generatorsystem"></a>Женераторсистем: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Объект `GeneratorSystem` , описывающий $H $ как сумму паулиных терминов



## <a name="output--doubleblockencodingreflection"></a>Выходные данные: ([Double](xref:microsoft.quantum.lang-ref.double),[блоккенкодингрефлектион](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))

## <a name="first-parameter"></a>Первый параметр

Один из норм коэффициентов $ \алфа = \ sum_ {j} | \ alpha_j | $.

## <a name="second-parameter"></a>Второй параметр

`BlockEncodingReflection`Единое $U $ хамилтониан $H $. Так как это единое значение соответствует $U ^ 2 = I $, это также отражение.

## <a name="remarks"></a>Комментарии

Это достигается путем подготовки и отменяя подготовку состояния $ \ sum_ {j} \скрт{\ alpha_j/\алфа}\кет{ж} $, а также конструирования единых <xref:microsoft.quantum.preparation.statepreparationpositivecoefficients> и <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> .