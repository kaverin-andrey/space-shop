> src
> > fonts - в этой папке лежат файлы шрифтов. Если добавили новый шрифт, необходимо удалить файл: scss/fonts/fonts.scss, и запустить сборку проекта npm run build

> > html - здесь лежат html файлы проекта

> > > _components - в папке лежат компоненты для переиспользования в другом месте(файл стилей компонента лежит в соответствующей папке /scss/_components/Имя_Компонента)
> > > index - в этой папке лежит основной код главной страницы

> > img - папка с изображениями проекта

> > js - основные скрипты
> > > modules - компоненты скриптов. 
> > > plugins - в этой папке лежат дополнительные плагины: swiper, скрипты bootstrap и пр.

> > scss
> > > _components - внутри папки
> > > _settings - основные настройки проекта, миксины, переменные, общие стили и пр.
> > > fonts - тут лежит файл стилей со шрифтами(Если добавили новый шрифт, процедуру по генерации нового файла описывал в выше в этом блоке)
> > > plugins - в этой папке лежат стили дополнительных плагинов: swiper, скрипты bootstrap и пр.
> > > templates - в этой папке будут лежать стили для отдельных страниц(одна папка - отдельная страница. Имя_папки = Имя_Страницы)

> > svgicons - в эту папку выгружаются иконки для создания svg спрайта
