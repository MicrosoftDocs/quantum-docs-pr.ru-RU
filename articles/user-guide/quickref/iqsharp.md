---
title: Магические команды IQ#
description: 'Краткая справочная страница для команд IQ # Magic с записными книжками Q # Jupyter'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
uid: microsoft.quantum.guide.quickref.iqsharp
ms.openlocfilehash: 0cd1a2289132e2760a21fd9d4f4083696353e271
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2020
ms.locfileid: "83431025"
---
# <a name="iq-magic-commands"></a><span data-ttu-id="030bc-103">Магические команды IQ#</span><span class="sxs-lookup"><span data-stu-id="030bc-103">IQ# Magic Commands</span></span>

### <a name="general"></a><span data-ttu-id="030bc-104">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="030bc-104">General</span></span>

- <span data-ttu-id="030bc-105">`%config`: Задает или получает параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="030bc-105">`%config`: Sets or gets configuration preferences.</span></span>
- <span data-ttu-id="030bc-106">`%estimate`: Выполняет заданную функцию или операцию на целевом компьютере Куантумсимулатор.</span><span class="sxs-lookup"><span data-stu-id="030bc-106">`%estimate`: Runs a given function or operation on the QuantumSimulator target machine.</span></span>
- <span data-ttu-id="030bc-107">`%lsmagic`— Возвращает список всех доступных в настоящее время команд Magic.</span><span class="sxs-lookup"><span data-stu-id="030bc-107">`%lsmagic`: Returns a list of all currently available magic commands.</span></span>
- <span data-ttu-id="030bc-108">`%package`— Предоставляет возможность загрузки пакета NuGet.</span><span class="sxs-lookup"><span data-stu-id="030bc-108">`%package`: Provides the ability to load a Nuget package.</span></span>
- <span data-ttu-id="030bc-109">`%performance`: Сообщает текущие метрики производительности для этого ядра.</span><span class="sxs-lookup"><span data-stu-id="030bc-109">`%performance`: Reports current performance metrics for this kernel.</span></span>
- <span data-ttu-id="030bc-110">`%simulate`: Выполняет заданную функцию или операцию на целевом компьютере Куантумсимулатор.</span><span class="sxs-lookup"><span data-stu-id="030bc-110">`%simulate`: Runs a given function or operation on the QuantumSimulator target machine.</span></span>
- <span data-ttu-id="030bc-111">`%toffoli`: Выполняет заданную функцию или операцию на целевом компьютере имитатора Тоффолисимулатор.</span><span class="sxs-lookup"><span data-stu-id="030bc-111">`%toffoli`: Runs a given function or operation on the ToffoliSimulator simulator target machine.</span></span>
- <span data-ttu-id="030bc-112">`%who`: Предоставляет действия, связанные с текущей рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="030bc-112">`%who`: Provides actions related to the current workspace.</span></span>
- <span data-ttu-id="030bc-113">`%workspace`: Возвращает список всех операций и функций, определенных в текущем сеансе, либо интерактивно, либо загруженных из текущей рабочей области.</span><span class="sxs-lookup"><span data-stu-id="030bc-113">`%workspace`: Returns a list of all operations and functions defined in the current session, either interactively or loaded from the current workspace.</span></span>

### <a name="chemistry"></a><span data-ttu-id="030bc-114">Химия</span><span class="sxs-lookup"><span data-stu-id="030bc-114">Chemistry</span></span>

- <span data-ttu-id="030bc-115">`%chemistry.broombridge`: Загружает и возвращает представление проблем с электронной структурой Брумбридже из заданного YAML-файла.</span><span class="sxs-lookup"><span data-stu-id="030bc-115">`%chemistry.broombridge`: Loads and returns Broombridge electronic structure problem representation from a given .yaml file.</span></span>
- <span data-ttu-id="030bc-116">`%chemistry.encode`: Кодирует фермион Хамилтониан в формат, который можно использовать в Q #.</span><span class="sxs-lookup"><span data-stu-id="030bc-116">`%chemistry.encode`: Encodes a fermion Hamiltonian to a format consumable by Q#.</span></span>
- <span data-ttu-id="030bc-117">`%chemistry.fh.add_terms`: Добавляет термины в фермион Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="030bc-117">`%chemistry.fh.add_terms`: Adds terms to a fermion Hamiltonian.</span></span>
- <span data-ttu-id="030bc-118">`%chemistry.fh.load`: Загружает Хамилтониан фермион для проблемы с электронной структурой.</span><span class="sxs-lookup"><span data-stu-id="030bc-118">`%chemistry.fh.load`: Loads the fermion Hamiltonian for an electronic structure problem.</span></span> <span data-ttu-id="030bc-119">Проблема загружается из файла или передается в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="030bc-119">The problem is loaded from a file or passed as an argument.</span></span>
- <span data-ttu-id="030bc-120">`%chemistry.inputstate.load`: Загружает ошибку электронной структуры Брумбридже и возвращает выбранное состояние входа.</span><span class="sxs-lookup"><span data-stu-id="030bc-120">`%chemistry.inputstate.load`: Loads Broombridge electronic structure problem and returns selected input state.</span></span>

### <a name="from-microsoftquantumkatas-package"></a><span data-ttu-id="030bc-121">Из пакета Microsoft. тактов. Катас</span><span class="sxs-lookup"><span data-stu-id="030bc-121">From Microsoft.Quantum.Katas package</span></span>

- <span data-ttu-id="030bc-122">`%kata`: Выполняет один тест и сообщает, успешно ли пройден тест.</span><span class="sxs-lookup"><span data-stu-id="030bc-122">`%kata`: Executes a single test, and reports whether the test passed successfully.</span></span>
- <span data-ttu-id="030bc-123">`%check_kata`: Проверяет эталонную реализацию для теста одного Ката.</span><span class="sxs-lookup"><span data-stu-id="030bc-123">`%check_kata`: Checks the reference implementation for a single kata's test.</span></span>
    <span data-ttu-id="030bc-124">В частности, он заменяет эталонную реализацию для отдельной задачи на ячейку и сообщает, успешно ли прошел тест.</span><span class="sxs-lookup"><span data-stu-id="030bc-124">Specifically, it substitutes the reference implementation for a single task into the cell, and reports whether the test passed successfully.</span></span>
