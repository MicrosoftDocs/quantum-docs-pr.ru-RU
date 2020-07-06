# <a name="articles"></a>Статьи

В этом каталоге содержатся статьи с документацией по пакету разработки тактов. Этот каталог содержит:

- **Каталоги статей**: содержат статьи для каждого раздела документации. В этих каталогах можно найти следующее содержимое:
  
  - Каждый каталог содержит `toc.yml` файл для просмотра содержимого каталога в основном содержании (TOC).
  - Markdown статьи, содержащие документацию. Эти статьи должны следовать указаниям руководства для [участников документация Майкрософт](https://docs.microsoft.com/en-us/contribute/).
  - Подкаталоги статей. Эти вложенные каталоги также должны содержать собственный `toc.yml` файл.

> :p енЦил: Несмотря на то, что можно ссылаться на `*.md` файлы непосредственно в родительском `TOC.yml` файле, чтобы они были упорядочены, они будут ссылаться только из `toc.yml` текущего каталога.

- **Основной `TOC.yml` файл оглавления (TOC)**. в этом файле разделы оглавления веб-сайта перечислены вместе со ссылкой на основной `toc.yml` файл каталога для каждого раздела.
- **`index.yml`** YAML с конфигурацией целевой страницы документации.
- **`\media`**: Каталог для хранения всех образов, используемых в документации. Он содержит `\media\src` подкаталог для хранения исходных файлов изображений.
- **Файлы лицензий**: файлы, содержащие юридические лицензии
- **Технические файлы**: файлы, содержащие макросы и метаданные.

## <a name="guidelines"></a>Рекомендации

Некоторые общие рекомендации по организации этого каталога для участников:

- Каждый каталог или вложенный каталог должен содержать собственный `toc.yml` файл, который ссылается на статьи того же уровня или на `toc.yml` файлы его дочерних каталогов.
- Организация каталогов репозитория должна быть максимально близкой к организации содержания веб-сайта документации.
- Все образы должны храниться в `articles\media` папке "статьи", а не в ней.
- Заголовки статей, имена в ОГЛАВЛЕНИи и *UID* метаданных должны быть максимально близко друг от друга и представлять собой заголовок H1 документа Markdown.

## <a name="adding-images"></a>Добавление изображений

Чтобы изображения были правильно отображены в темном режиме, необходимо избежать прозрачности.
- Для `*.jpg` файлов не нужно ничего делать, так как формат файла не поддерживает прозрачные элементы.
- Для `*.png` файлов необходимо добавить белый фон или изменить значение альфа-канала на 100. Самый простой способ сделать это в Windows — открыть файл в Paint и сохранить его, перезаписав исходный файл.
- Для `*.svg` файлов необходимо добавить белый прямоугольник на самом низком слое. Это можно сделать с помощью Inkscape:
  - Откройте файл `*.svg` .
  - Выберите инструмент Square Maker и нарисуйте белый прямоугольник поверх исходного рисунка.
  - Выберите инструмент "выбор и преобразование объектов", щелкнув кнопку с темной стрелкой или нажав клавишу F1.
  - Выполняя выделение прямоугольника, щелкните элемент панели инструментов "Нижний выбор в нижней части (конец)".
  - Настройте прямоугольник с помощью мыши или клавиш со стрелками.