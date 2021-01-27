---
uid: Microsoft.Quantum.Simulation.PauliBlockEncoding
title: Функция Паулиблоккенкодинг
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: 2e37b40c60d19aa747114de988dddc19f0d7c50b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848008"
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

## <a name="remarks"></a>Remarks

Это достигается путем подготовки и отменяя подготовку состояния $ \ sum_ {j} \скрт{\ alpha_j/\алфа}\кет{ж} $, а также конструирования единых <xref:microsoft.quantum.preparation.statepreparationpositivecoefficients> и <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> .