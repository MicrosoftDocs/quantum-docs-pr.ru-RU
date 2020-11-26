---
uid: Microsoft.Quantum.Simulation._PauliBlockEncoding
title: Функция _PauliBlockEncoding
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: 6ad3e692f68ec2d405e19a7e467ef8fe33d449fc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225573"
---
# <a name="_pauliblockencoding-function"></a>Функция _PauliBlockEncoding

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Создает единое блочное кодирование для Хамилтониан.

Хамилтониан $H = \ sum_ {j} \ alpha_j P_j $ описывается суммой Паулиных терминов $P _j $, каждый с действительным коэффициентом $ \ alpha_j $.

```qsharp
function _PauliBlockEncoding (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem, statePrepUnitary : (Double[] -> (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)), multiplexer : ((Int, (Int -> (Qubit[] => Unit is Adj + Ctl))) -> ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))) : (Double, Microsoft.Quantum.Simulation.BlockEncodingReflection)
```


## <a name="input"></a>Входные данные

### <a name="generatorsystem--generatorsystem"></a>Женераторсистем: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Объект `GeneratorSystem` , описывающий $H $ как сумму паулиных терминов


### <a name="stateprepunitary--double---littleendian--unit--is-adj--ctl"></a>статепрепунитари: [Double](xref:microsoft.quantum.lang-ref.double)[]-> [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [ед](xref:microsoft.quantum.lang-ref.unit)  .

Единая операция $V $, которая применяет единое $V _j $ под управлением индекса $ \кет{ж} $, учитывая функцию $f: ж\ригхтарров V_j $.


### <a name="multiplexer--intint---qubit--unit--is-adj--ctl---littleendianqubit--unit--is-adj--ctl"></a>Мультиплексор: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> [кубит](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL") — > ([литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"





## <a name="output--doubleblockencodingreflection"></a>Выходные данные: ([Double](xref:microsoft.quantum.lang-ref.double),[блоккенкодингрефлектион](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))

## <a name="first-parameter"></a>Первый параметр

Один из норм коэффициентов $ \алфа = \ sum_ {j} | \ alpha_j | $.

## <a name="second-parameter"></a>Второй параметр

`BlockEncodingReflection`Единое $U $ хамилтониан $U $. Так как это единое значение соответствует $U ^ 2 = I $, это также отражение.

## <a name="remarks"></a>Комментарии

Примерами операций подготовка и отменяющая подготовка состояния $ \ sum_ {j} \скрт{\ alpha_j/\алфа}\кет{ж} $ и создание единого с учетом умножения <xref:microsoft.quantum.canon.statepreparationpositivecoefficients> <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> .