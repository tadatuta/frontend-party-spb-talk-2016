---

layout: default

---

# Яндекс

## **{{ site.presentation.title }}** {#cover}

<div class="s">
    <div class="service">{{ site.presentation.service }}</div>
</div>

{% if site.presentation.nda %}
<div class="nda"></div>
{% endif %}

<div class="info">
	<p class="author">{{ site.author.name }}, <br/> {{ site.author.position }}</p>
</div>

## О чём речь

* Сборка проекта при компонентном подходе
* ...Композиция. Зависимости между компонентами
* ...Уровни переопределения
* ...Алгебра деклараций

## **Этот подход применим без блоков, элементов, модификаторов**

## Копонентный подход

* [Bootstrap](https://github.com/twbs/bootstrap/tree/master/less)
* ...[БЭМ](https://github.com/bem/bem-components/tree/v2/common.blocks)
* ...[React](https://github.com/callemall/material-ui/tree/master/src)
* ...[Web Components](https://github.com/PolymerElements)

## Сборка при компонентном подходе

* Найти все компоненты на FS
* ...Написать require/import в каждой технологии

## Найти все компоненты на FS

* Собираем лишнее
* ...Не можем гарантировать порядок

## Написать require/import в каждой технологии

* Много ручной работы
* ...Вербозно
* ...Мухи и котлеты

## **![](pictures/exit.jpg)**
{:.cover}

## Декларируем бандл в терминах компонентов

* Не говорим, где физически находятся файлы
* ...Не говорим, какие технологии нам нужны

## Было

index.css

~~~ css
@import "../../path/to/component/component.css";
@import "../../path/to/component2/component2.css";
/* project styles */
~~~

index.js

~~~ js
require(../../path/to/component/component.js);
require(../../path/to/component2/component2.js);
/* project logic */
~~~

## Стало

index.decl.js

~~~ js
['component', 'components2']
~~~

## Композиция. Зависимости между компонентами

* Зависимости как технология компонента

## Было

my-component.css

~~~ css
@import "../../path/to/component/component.css";
@import "../../path/to/component2/component2.css";
/* my-component styles */
~~~

my-component.js

~~~ js
require(../../path/to/component/component.js);
require(../../path/to/component2/component2.js);
/* my-component logic */
~~~

## Стало

my-component.deps.js

~~~ js
['component', 'components2']
~~~

## **Уровни переопределения**

## **![](pictures/levels.png)**
{:.cover}

## Уровни переопределения

~~~ css
.button {
    width: 200px;
    color: red;
}
~~~

## Уровни переопределения

~~~ css
.button {
    width: 200px;
    color: red;
}

.button {
    height: 50px;
    color: green;
}
~~~

## **Алгебра деклараций**

## Алгебра деклараций

* Сложение
* Вычитание
* Пересечение

## **[Как это работает](https://github.com/bem/project-stub/tree/preparing-for-master)**

## **Ваши вопросы!**

## **Контакты** {#contacts}

<div class="info">
<p class="author">{{ site.author.name }}</p>
<br>
<!-- <p class="position">{{ site.author.position }}</p> -->

    <div class="contacts">
        <p class="contacts-left contacts-top">bem.info</p>
        <p class="contacts-left mail">info@bem.info</p>
        <p class="contacts-right twitter">bem_ru&nbsp;&nbsp;&nbsp;&nbsp;#b_</p>
        <!-- <p class="contacts-right contacts-bottom vk">vk</p> -->
        <!-- <p class="contacts-right facebook">facebook</p> -->
    </div>
</div>
