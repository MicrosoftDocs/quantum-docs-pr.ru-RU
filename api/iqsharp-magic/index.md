# <a name="iq-magic-commands"></a>Магические команды IQ#

| Магические команды | Сводка |
|---------------|---------|
| [`%check_kata`](xref:microsoft.quantum.iqsharp.magic-ref.check_kata) | Проверяет эталонную реализацию теста для одного задания. |
| [`%chemistry.broombridge`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.broombridge) | Загружает и возвращает представление проблемы, связанной с электронной структурой Брумбриджа, из заданного YAML-файла. |
| [`%chemistry.encode`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.encode) | Кодирует гамильтоново представление фермиона в формат, поддерживаемый в Q#. |
| [`%chemistry.fh.add_terms`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.add_terms) | Добавляет условия в гамильтоново представление фермиона. |
| [`%chemistry.fh.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.load) | Загружает гамильтоново представление фермиона для проблемы, связанной с электронной структурой. Проблема загружается из файла или передается в качестве аргумента. |
| [`%chemistry.inputstate.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.inputstate.load) | Загружает проблему, связанную с электронной структурой Брумбриджа, и возвращает состояние выбранного входа. |
| [`%config`](xref:microsoft.quantum.iqsharp.magic-ref.config) | Разрешает настройку или запрашивание параметров конфигурации. |
| [`%estimate`](xref:microsoft.quantum.iqsharp.magic-ref.estimate) | Выполняет заданную функцию или операцию на целевом компьютере ResourcesEstimator. |
| [`%kata`](xref:microsoft.quantum.iqsharp.magic-ref.kata) | Выполняет один тест. |
| [`%lsmagic`](xref:microsoft.quantum.iqsharp.magic-ref.lsmagic) | Возвращает список всех доступных магических команд. |
| [`%package`](xref:microsoft.quantum.iqsharp.magic-ref.package) | Разрешает загружать пакет NuGet. Пакет должен быть доступным в списке источников NuGet (обычно это nuget.org). |
| [`%performance`](xref:microsoft.quantum.iqsharp.magic-ref.performance) | Предоставляет текущие метрики производительности для этого ядра. |
| [`%simulate`](xref:microsoft.quantum.iqsharp.magic-ref.simulate) | Выполняет заданную функцию или операцию на целевом компьютере QuantumSimulator. |
| [`%toffoli`](xref:microsoft.quantum.iqsharp.magic-ref.toffoli) | Выполняет заданную функцию или операцию на целевом компьютере ToffoliSimulator. |
| [`%who`](xref:microsoft.quantum.iqsharp.magic-ref.who) | Предоставляет действия, связанные с текущей рабочей областью. |
| [`%workspace`](xref:microsoft.quantum.iqsharp.magic-ref.workspace) | Возвращает список всех операций и функций, определенных в текущем сеансе, интерактивно или после загрузки из текущей рабочей области. |
