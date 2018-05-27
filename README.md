# 1.2 Списки и таблицы

## Списки
Спи́сок в типографике — способ оформления различного рода перечислений или перечней. Каждый элемент списка начинается с маркера списка или номера-буквы, и весь текст списка не должен выступать влево за них.

Списки могут быть:

 * упорядоченные или неупорядоченные.
Если последовательность перечисленных элементов не зависит от какого-то определенного логического порядка, то такой список является упорядоченным. Если же от перестановки перечисленных элементов изменяется смысл, то такой список называется упорядоченным;
 * нумерованные и ненумерованные.
Каждый элемент нумерованного списка начинается с порядкового номера или буквы в алфавитном порядке. Элемент ненумерованного списка начинается c маркера списка;
 * одноуровневые (простые) или многоуровневые.

[Ссылка на Вики](https://ru.wikipedia.org/wiki/%D0%A1%D0%BF%D0%B8%D1%81%D0%BE%D0%BA_%28%D1%82%D0%B8%D0%BF%D0%BE%D0%B3%D1%80%D0%B0%D1%84%D0%B8%D0%BA%D0%B0%29)

### Виды списков
В вебе выделяют три основных вида списков: 

 1. Маркированные списки
 2. Нумерованные списки
 3. Списки описаний

Разница между ними в смысловой нагрузке. Правильно подбирайте список исходя из контента.

Если в списке важна последовательность действий, например расписание занятий на день, то вам подойдут нумерованные списки.  
Если нужно перечислить несколько пунктов без четкой их последовательности, например, список покупок, то можно выбрать маркированный список.  
В случае, когда требуется оформить несколько определений и дать им описание, подойдет список описаний. 

У списков есть стили по умолчанию. Визуально текст отбивается пустой строкой до начала и пустой строкой после окончания. Поэтому в тексте он выделяется.  
Все пункты списка визуально немного смещены относительно левого края всего остального текста, и перед каждым пунктом появляется либо маркер (по умолчанию черная точка), либо номер. Это привлекает внимание читателя к тексту и повышает его читабельность.

### Синтаксис
#### Общее 
Во всех видах списков общим является то, что вложить внутрь родительского тега можно только теги пунктов списка. Внутрь тегов пунктов списка уже можно вкладывать какие угодно теги, в том числе и другие списки.

#### Маркированные списки
##### Ненумерованный список

*ul* — родительский тег. Все списки начинаются с него. Это парный тег.  
*UL* = Unordered List — неупорядоченный список.  
*li* — тег пункта списка. Парный тег.  
*LI* = List Item — элемент списка.

Пример структуры простого маркированного списка. 

Представим ситуацию: нам на странице нужно перечислить список продуктов, которые понадобятся, чтобы приготовить пиццу.  
Мы понимаем, что нам нужно использовать список — так будет нагляднее и понятнее, чем перечислить все в строку. А также будет удобно распечатать страницу и отмечать то, что уже есть.  
Какой список выбрать? В этом случае порядок покупки продуктов не важен. Главное — перечислить их все. Значит, подойдет маркированный список.  
Отлично. На странице в тексте, где должен быть список, мы добавляем родительский тег списка. Поскольку список маркированный, то это будет `ul`.  
Каждый продукт должен идти отдельным пунктом списка. Это значит, что каждый продукт мы должны разместить между `<li>` и `</li>` — в тексте напротив поставится точка, и после будет перенос строки.  
Когда наш список закончен — закрываем его при помощи тега `</ul>`

В итоге разметка для нашего списка покупок будет выглядеть так. (показать результат)

    <ul> 
      <li>Тесто для пиццы</li> 
      <li>Начинка</li> 
      <li>Соус</li> 
      <li>Сыр</li> 
    </ul>

##### Нумерованный список

*ol* — родительский тег. Парный тег.  
*OL* = Ordered List — упорядоченный список.  
*li* — тег пункта списка.  

Пример структуры простого списка.

Продолжим писать контент для страницы о приготовлении пиццы. Теперь нам нужно оформить рецепт приготовления. Очевидно, что тут нам тоже пригодится список.  
Действия обязательно делать в определенном порядке, нельзя положить тесто сверху на сыр. Значит, нам нужен нумерованный список.  
Как и в предыдущем случае, каждое действие нужно разместить в отдельном пункте списка, чтобы напротив автоматически проставилась цифра.

В нужном месте текста обозначаем что здесь будет список — открываем тег `<ol>`.  
Дальше размещаем все нужные нам пункты, оборачивая текст в теги `<li>`.

Значит, наша разметка будет выглядеть следующим образом (показать результат):

    <ol> 
      <li>Включить духовку на разогрев</li>
      <li>Раскатать тесто толщиной 5мм</li>
      <li>Выложить соус и начинку</li>
      <li>Посыпать сыром</li>
      <li>Поставить в духовку на 7 минут</li>      
    </ol>

#### Списки описаний

В этом типе списков структура чуть сложнее, чем у предыдущих. Здесь используются три тега: родительский, тег термина и тег определения. 

*dl* — родительский парный тег.  
*DL* = Description List — список описаний.  
*dt* — тег, в который заключается термин, парный.  
*DT* = Definition Term — термин.  
*dd* — тег, в котором размещается определение для термина.  
*DD* = Description — описание.

Пример структуры простого списка.

Теперь мы хотим разобраться с видами пиццы и начинок для нее. У пиццы есть общепринятые названия, нам нужно дать расшифровку каждого. Для этого отлично подойдет список описаний.  
В нужном месте текста мы обозначаем, что здесь будет список. Открываем тег `<dl>`.  
Далее нам нужно написать название пиццы. Для этого используем тег термина и помещаем внутрь наше слово. Вот так `<dt>Пепперони</dt>`.  
После мы даем расшифровку этого термина и пишем внутри тега `dd`.

В итоге у нас получится такая структура (показать результат):

    <dl>
      <dt>Пепперони</dt>
      <dd>Пицца, главный ингредиент которой это одноименная острая вяленая колбаса «Пепперони».</dd>
      <dt>Маргарита</dt>
      <dd>Лаконичная пицца, которая содержит только томаты, сыр и базилик.</dd>
      <dt>Гавайская</dt>
      <dd>Пицца с ананасом для тех, кто понимает.</dd>
    </dl>

#### Изменяем нумерацию упорядоченного списка
Вернемся к нашему списку действий в рецепте приготовления. Важно отметить, что начинка должна быть уже готовой к употреблению.

Мы понимаем, что нам нужно разорвать список, вставить текст, а потом снова продолжить список. (показать пример)  
Если мы просто разорвем список, а потом откроем новый, то второй список снова начнется с единицы. Что же делать?

Нужно начать нумерованный список не с единицы. На этот случай вы можете использовать html-атрибут `start`.


    <ol> 
      <li>Включить духовку на максимальную мощность</li>
      <li>Раскатать тесто толщиной 5мм</li>
      <li>Выложить соус и начинку</li>
    </ol>
    <p>Пицца печется очень быстро, сырые продукты не успеют приготовиться. Начинка должна быть готовой.</p>
    <ol start="4">
      <li>Выложить сыр</li>
      <li>Поставить пиццу в духовку на 7 минут</li>
    </ol>


В качестве значения атрибута указываем число, с которого нужно начать этот конкретный список. 

#### Многоуровневые списки
Отдельно стоит остановится на списках, состоящих из нескольких уровней.

В процессе создания многоуровнего списка стоит помнить о правиле, что в списке могут быть только пункты списка. 
Это значит, что второй и все следующие уровни списка нужно поместить  внутрь пункта предыдущего списка. 

Вы можете комбинировать нумерованные и маркированные списки при вложении.

Давайте приведем примеры начинок, чтобы не растеряться в магазине. Мы понимаем, что нам нужно поместить список в список. Ингредиенты можно брать в любом порядке, поэтому можно отразить их при помощи маркированного списка.  

Чтобы создать второй уровень списка, в нужном пункте первого списка мы открываем новый список. В нашем случае это ненумерованный список — используем `<ul>`.  
Дальше размещаем информацию об ингредиентах — каждый продукт в новый пункт.  
Когда все необходимое перечислено — закрываем второй уровень списка — `</ol>`.  
И теперь закрываем пункт первого списка — `</li>`.

Результат:

    <ul> 
      <li>Тесто для пиццы</li> 
      <li>Начинка на выбор:
	      <ul>
		      <li>Томаты;</li>
		      <li>Маринованные огурцы;</li>
		      <li>Колбаса;</li>
		      <li>Грибы;</li>		      		      		      
		      <li>Маслины.</li>		      
	      </ul>
      </li> 
      <li>Соус</li> 
      <li>Сыр</li> 
    </ul>

## Таблицы
Нужно подсчитать, сколько денег было потрачено на приготовление пиццы. На странице должны быть следующие данные: название продукта, страна производитель, стоимость.

Мы понимаем, что списком такую информацию не оформишь, будет очень неудобно, например, считать итоговую сумму.

Лучше всего для этих целей подойдет таблица. Все данные о продукте находятся в одной строке — удобно искать и считать. Каждая колонка в таблице может иметь заголовок — просто будет определить, что значит текст/цифра, расположенные в ячейке.

### Синтаксис
Таблица всегда состоит из строк и ячеек в строке. 

В нужном месте страницы мы создаем таблицу при помощи парного родительского тега *table*.  
Затем внутрь таблицы помещается необходимое количество строк при помощи парного тега *tr*. *TR* расшифровывается как *table row* — срока таблицы.  
В каждой строке может лежать любое (нужное вам) количество ячеек. Ячейки бывают двух типов: 

* *th* — для заголовков колонки. *TH — table header cell* — ячейка «шапки» таблицы. Текст в такой ячейке отображается жирным шрифтом и выравнивается по центру.  
* *td* - для всех остальных ячеек. *TD — table data cells* — ячейка данных таблицы.

Сколько ячеек вы разместите в ряду, столько колонок у вас получится. Важно помещать одинаковое количество ячеек в каждую строку для правильного внешнего вида таблицы и состыковки данных по вертикали и горизонтали. 

#### Стандартная структура 
Давайте разместим данные в таблице. Всего из магазина мы принесли 6 различных продуктов. Это значит, что нам нужно создать 6 строк. 

Открываем таблицу при помощи родительского тега `table` и размещаем внутри 6 строк — тегов `tr`. Внутри строк ничего писать не нужно. Все данные будут лежать в ячейках, находящихся в строке.

    <table>
	    <tr></tr>
	    <tr></tr>
	    <tr></tr>
	    <tr></tr>	    
	    <tr></tr>
	    <tr></tr>
	    <tr></tr>
	    <tr></tr>	    
    </table>

Далее в каждой строке нам нужно создать 3 ячейки — с названием продукта, страной, стоимостью:  
[https://codepen.io/wizjer/pen/QrRBPO?editors=1000](https://codepen.io/wizjer/pen/QrRBPO?editors=1000) 

И, наконец, заполним таблицу данными:  
[https://codepen.io/wizjer/pen/NMVBQa?editors=1000](https://codepen.io/wizjer/pen/NMVBQa?editors=1000) 

#### Заголовки колонок
Отлично, мы внесли данные в таблицу. Но через неделю нам уже не вспомнить, что за цифра в последней колонке — масса это или цена? Нужно подписать колонки и обозначить, что за данные в каждой из них находятся.

Чтобы создать строку с заголовками колонок и отделить эту строку от основных данных таблицы используется парный тег *thead* — `table head`.  
*thead* следует использовать в самом начале таблицы. Что логично, поскольку заголовки колонок должны располагаться сверху. Допускается использование не более одного *thead* в пределах одной таблицы.  
Тег должен идти в разметке сразу после тега `table`. Внутрь вкладывается тег ряда — `tr`, а в него теги ячеек — `td`.

Давайте зададим заголовки нашим колонкам:  
[https://codepen.io/wizjer/pen/ELzeVz?editors=1000](https://codepen.io/wizjer/pen/ELzeVz?editors=1000)  

#### Тело таблицы
После `thead` должен идти основной контент таблицы. Его так же группируют по смыслу, для этого используется парный тег `tbody` — table body.  
Тел таблицы может быть много. Например, мы можем разбить продукты по магазинам, где они были куплены.

[https://codepen.io/wizjer/pen/wjbEpm?editors=1000](https://codepen.io/wizjer/pen/wjbEpm?editors=1000) 

Теперь нам нужно подвести итог и посчитать, сколько всего было потрачено денег. 

Вы наверняка не раз видели таблицы с расчетами, где в нижней строке выводится сумма или какой-то вывод из приведенных выше цифр. Именно для таких строк ИТОГО используется парный тег `tfoot` — table footer. Синтаксис его использования ничем не отличается от предыдущих логических элементов `thead` и `tbody`. 

Давайте подсчитаем и выведем общую сумму:  
[https://codepen.io/wizjer/pen/bMyxLM?editors=1000](https://codepen.io/wizjer/pen/bMyxLM?editors=1000) 

#### Атрибуты
Мы видим, что в строках с названиями магазинов у нас есть пустые ячейки. Та же ситуация в последней строке ИТОГО. Почему бы не объединить пустые ячейки? Так таблица станет более читаемой. 

Что делать, если нам нужно объединить несколько ячеек по горизонтали?  
Без паники! Все придумано до нас. Для этих целей используются специальные html-атрибуты `colspan`.  

`span` дословно переводится как «охват». Это хорошо объясняет, что именно делают атрибуты.  
Если мы укажем у тега `td` атрибут `colspan` и в значении напишем 3, то ячейка растянется, охватит собою место под 3 ячейки.  
Значением этих атрибутов может быть только целое положительное число.

Так как одна ячейка может занимать несколько позиций в строке или в столбце, или и там и там одновременно, то важно следить за суммарным количеством ячеек в строках и столбцах с учетом охвата.

Это схоже с тем, как работает кнопка ![button](res/button.png) в Excel.

Пример с использованием `colspan`.

Давайте объединим пустые ячейки в строках с названиями магазинов и в последней строке с итоговым количеством баллов:  
[https://codepen.io/wizjer/pen/ZoNMLw?editors=1000](https://codepen.io/wizjer/pen/ZoNMLw?editors=1000) 

Поскольку все купленные на рынке продукты приехали к нам из Казахстана, то мы можем объединить обе ячейки в одну по высоте. Для этого используется атрибут `rowspan`:  
[https://codepen.io/wizjer/pen/jxovdd?editors=1000](https://codepen.io/wizjer/pen/jxovdd?editors=1000) 

Как вы, возможно, заметили, в строках не хватает ячеек. Причина в том, что для охвата нужно будет освободить место. По факту атрибуты не склеивают ячейки по ширине или высоте. Они растягивают одну ячейку на указанное количество строк или колонок. Соответственно, для того чтобы таблица не развалилась, нужно освободить место под это растягивание. 

Ура! Мы отлично справились с контентом на странице о приготовлении пиццы. А также выучили три вида списков и таблицы.
