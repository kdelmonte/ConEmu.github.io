---
title: "ConEmu | Working with touchscreen"

description: "If you have touch-sensitive screen, you may use ‘taps’ and ‘gestures’ in ConEmu-Maximus5"

breadcrumbs:
 - url: TableOfContents.html#controls
   title: Controls

otherlang:
   eng: /en/TabletPC.html
   rus: /ru/TabletPC.html
---

# Working with touchscreen

If you have touch-sensitive screen, you may use ‘taps’ and ‘gestures’ in ConEmu-Maximus5.

[Far Manager](FarManager.html) users may use [extended](#FarManager) gesture list.

This article describes Windows 8 gestures.


<h2 id="Terms"> Terms </h2>

| Name | Description |
|:---|:---|
| Тап пальцем | Нажать-отпустить. |
| Тап двумя пальцами | Одновременно двумя пальцами нажать-отпустить. «Точкой применения» считается центр между точками касания. |
| Двойной тап пальцем | Нажать-отпустить-нажать-отпустить. |
| Двойной тап с удержанием пальца | Нажать-отпустить-нажать-ждать-отпустить |
| Длинный тап | Нажать одним пальцем, держать, пока под пальцем не появится «квадрат», после этого палец отпустить. |
| Прокрутка | Одновременно двумя пальцами нажать-перетащить-отпустить. |
| Перетаскивание | Нажать одним пальцем-перетащить-отпустить. |
| Поворот | Удерживая один палец вести другой по окружности вокруг первого |
| Масштаб | Нажать двумя пальцами и сводить/разводить их |


<h3 id="#Analogues"> Аналогии </h3>

| Mouse | Touch-screen |
|:---|:---|
| Клик левой кнопкой мышки | Тап пальцем |
| Двойной клик левой кнопкой мышки | Двойной тап пальцем |
| Клик правой кнопкой мышки | Длинный тап. В панелях Far Manager длинный тап отображает контекстное меню. |
| Драг левой кнопкой мышки | Перетаскивание: нажать одним пальцем-перетащить-отпустить |
| Драг правой кнопкой мышки | Нажать одним пальцем, держать, пока под пальцем не появится «квадрат», после этого перетащить и палец отпустить |



<h2 id="ConsoleScroll"> Console scrolling </h2>

* Одновременно двумя пальцами нажать-перетащить вверх/вниз-отпустить.

Так (а не одним пальцем) сделано потому, что многие консолные приложения
сами умеют обрабатывать события от «мышки», а «тап» и «перетаскивание»
преобразуются в «обычные» мышиные нажатия и перетаскивания.


<h2 id="TabSwitch"> Tab switching </h2>

* Жест "Поворот" листает табы влево/вправо.


<h2 id="FontScale"> Font size changing </h2>

* Жест "Масштаб" увеличивает/уменьшает размер шрифта.



<h2 id="FarManager"> How to use Far on TabletPC </h2>

<h3 id="FarSelectFile"> Files selection </h3>

<h4 id="FarSelectFileSingle"> Single </h4>

* Тап двумя пальцами. Для целкости попадания рекомендую две точки касания располагать по горизонтали (вдоль имени файла). Длинный тап - показ контекстного меню.
  * Держать палец над файлом/папкой, пока под пальцем не появится «квадрат». 
  * Палец можно отпускать - файл/папка выделится. 
  * Это аналог щелчка правой кнопкой пыши. 


<h4 id="FarSelectFileMulti"> Multiple </h4>

* Держать палец над первым файлом/папкой, пока под пальцем не появится «квадрат». После этого можно вести палец по панели - будут выделены «проведенные» элементы.
* Выделить/снять выделение с первого файла группы (тап двумя пальцами). После этого, на области статуса (для выделения вниз) или области имен колонок (для выделения вверх) двойной тап с удержанием.


<h3 id="FarPanelScroll"> Far Panel scrolling </h3>

* Прокрутка (одновременно двумя пальцами нажать-перетащить вверх/вниз-отпустить).
* Двойной тап с удержанием на заголовке колонки панели или статусной области приводит к прокрутке панели. Внимание! При этом может меняться «выделенность» элементов панели.


<h3 id="FarPanelResize"> Far Panels resizing </h3>

* Перетащите разделитель между панелями вправо/влево и отпустите. Внимание! На вкладке «Far Manager» должны быть включены флажки «Resize panels by mouse» и «use both panel edges».


<h3 id="FarPanelShowHide"> Show/hide Far Panels </h3>

* Тап по области часов +1 строка вниз (правый верхний угол). Аналог левому клику мышкой в координате {0,0}.


<h3 id="FarPanelEMenu"> Panels context menu - EMenu </h3>

{% comment %}
!!! проверить параметры настройки
{% endcomment %}

* Длинный тап. Должна быть включена настройка


<h3 id="FarViewerScroll"> Far Viewer scrolling </h3>

* Двойной тап по верхней/нижней части вьювера приводит к прокрутке содержимого вверх/вниз.


<h3 id="FarEditor"> Far Editor </h3>

* Удобно использовать макрос `Editor.MsRClick.lua` для копирования и вставки из буфера.
  Длинный тап по редактору или полю редактирования в диалоге приводит к отображению меню,
  выделив слово под курсором (под местом тапа).

~~~
------------------------¬
¦  Copy whole line      ¦
¦  Copy single word     ¦
¦  Paste from clipboard ¦
L------------------------
~~~

*В диалогах пункт "Copy single word" отсутствует.*
