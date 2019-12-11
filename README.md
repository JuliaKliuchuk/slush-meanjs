# slush-meanjs [![Build Status](https://secure.travis-ci.org/arvindr21/slush-meanjs.png?branch=master)](https://travis-ci.org/arvindr21/slush-meanjs) [![NPM version](https://badge-me.herokuapp.com/api/npm/slush-meanjs.png)](http://badges.enytc.com/for/npm/slush-meanjs) [![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/arvindr21/slush-meanjs/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

[![NPM](https://nodei.co/npm/slush-meanjs.png?downloads=true&stars=true)](https://nodei.co/npm/slush-meanjs/)

> A slush generator to scaffold MEAN Apps

## ** Этот проект больше не находится под активным обслуживанием, если кто-то заинтересован в управлении этим, пожалуйста, свяжитесь со мной **

Вдохновленный [MEAN](http://meanjs.org/)

## Начало работы

### Установка

Установка `slush-meanjs` глобально:

```bash
$ npm install -g slush-meanjs
```

Не забудьте также установить `gulp` и` slush` глобально, если вы этого еще не сделали:

```bash
$ npm install -g gulp slush
```

### Использование

Создайте новую папку для вашего проекта:

```bash
$ mkdir my-slush-meanjs
```

Запустите генератор из новой папки:

```bash
$ cd my-slush-meanjs && slush meanjs
```
## Запуск приложения

Чтобы запустить приложение, сначала убедитесь, что mongoDB запущен (```$ mongod```), затем

```bash
$ gulp
```
и перейдите к ```http://localhost:3000```


Чтобы сгенерировать минимизированные файлы js & css в папке `public / dist`, запустите

```bash
$ gulp build
```

To lint files

```bash
$ gulp lint
```

Запуск тестов

```bash
$ gulp test
```

## FEATURES
<table>
<tr>
<td>Feature</td>
<td>Command</td>
</tr>
<tr>
<td><a href="#application-generator">MEAN Application generator</a></td>
<td>slush meanjs</td>
</tr>
<tr>
<td><a href="#crud-module-sub-generato">CRUD Module sub-generator</a></td>
<td>slush meanjs:crud-module {{module-name}}</td>
</tr>
<tr>
<td><a href="#angularjs-module-sub-generator">AngularJs Module sub-generator</a></td>
<td>slush meanjs:angular-module {{module-name}}</td>
</tr>
<tr>
<td><a href="#angularjs-route-sub-generator">AngularJs Route sub-generator</a></td>
<td>slush meanjs:angular-route {{route-name}}</td>
</tr>
<tr>
<td><a href="#angularjs-controller-sub-generator">AngularJs Controller sub-generator</a></td>
<td>slush meanjs:angular-controller {{controller-name}}</td>
</tr>
<tr>
<td><a href="#angularjs-view-sub-generator">AngularJs View sub-generator</a></td>
<td>slush meanjs:angular-view {{view-name}}</td>
</tr>
<tr>
<td><a href="#angularjs-service-sub-generator">AngularJs Service sub-generator</a></td>
<td>slush meanjs:angular-service {{service-name}}</td>
</tr>
<tr>
<td><a href="#angularjs-directive-sub-generator">AngularJs Directive sub-generator</a></td>
<td>slush meanjs:angular-directive {{directive-name}}</td>
</tr>
<tr>
<td><a href="#angularjs-filter-sub-generator">AngularJs Filter sub-generator</a></td>
<td>slush meanjs:angular-filter {{filter-name}}</td>
</tr>
<tr>
<td><a href="#angularjs-config-sub-generator">AngularJs Config sub-generator</a></td>
<td>slush meanjs:angular-config {{config-name}}</td>
</tr>
<tr>
<td><a href="#angularjs-test-sub-generator">AngularJs Test sub-generator</a></td>
<td>slush meanjs:angular-test {{controller-name}}</td>
</tr>
<tr>
<td><a href="#express-model-sub-generator">Express Model sub-generator</a></td>
<td>slush meanjs:express-model {{model-name}}</td>
</tr>
<tr>
<td><a href="#express-controller-sub-generator">Express Controller sub-generator</a></td>
<td>slush meanjs:express-controller {{controller-name}}</td>
</tr>
<tr>
<td><a href="#express-routes-sub-generator">Express Routes sub-generator</a></td>
<td>slush meanjs:express-route {{route-name}}</td>
</tr>
<tr>
<td><a href="#express-test-sub-generator">Express Test sub-generator</a></td>
<td>slush meanjs:express-test {{model-name}}</td>
</tr>
</table>

**Примечание. Генераторы должны запускаться из корневого каталога вашего приложения (app).**

## Application Generator

Генератор приложений поможет вам создать свежую копию приложения MEAN.JS в вашей рабочей папке. Чтобы создать приложение MEAN, перейдите в новую папку проекта, а затем используйте *slush meanjs* для создания приложения:

```
$ slush meanjs
```
Генератор задаст вам несколько вопросов о вашем новом приложении и сгенерирует его для вас. Когда процесс установки закончится, вы сможете использовать gulp для запуска вашего нового приложения MEAN:

```
$ gulp
```
Теперь генератор приложений отлично справляется с работой по созданию целого приложения, но ежедневная работа требует от нас повторения большого количества структурированного кода. Для этой цели мы предоставили вам несколько sub-generator, которые помогут вам ускорить разработку.

## CRUD Module Sub-Generator

Sub-generator модуля CRUD поможет вам создать новый модуль CRUD, подобный примеру статьи, поставляемому с проектом. Для создания нового модуля CRUD вам нужно будет снова использовать *slush meanjs* :
```
$ slush meanjs:crud-module <module-name>
```
Это создаст файлы AngularJS и Express, поддерживающие полную функциональность CRUD, и добавит тесты Karma и Mocha.

**Примечание:** Не забудьте использовать имя вашего модуля в качестве аргумента при вызове sub-generator модуля CRUD.


## AngularJS Module Sub-Generator

Другая избыточная задача - создание новой структуры модуля AngularJS. Для этого вы можете использовать Angular генератор sub-generator. Это создаст правильную структуру папок для вас и файла инициализации модуля. Создать новый модуль AngularJS просто:

```
$ slush meanjs:angular-module <module-name>
```

Sub-generator запросит дополнительную информацию о структуре вашей папки и создаст пустой новый модуль AngularJS. Теперь, чтобы заполнить этот новый модуль вашей бизнес-логикой, мы предоставили вам несколько sub-generator сущностей AngularJS.


## AngularJS Route Sub-Generator

Для создания вашего модуля вам часто нужно будет создать новый маршрут. Sub-generator маршрутов AngularJS поможет вам создать представление, контроллер и правильный маршрут в файле вашего модуля **rout.js**. Если он не может найти файл маршрутов модуля, sub-generator создаст его для вас. Создание нового маршрута AngularJS потребует выполнения этой команды:


```
$ slush meanjs:angular-route <route-name>
```

Sub-generator запросит дополнительную информацию о вашем контроллере, просмотре и маршрутизации URL и сгенерирует соответствующие файлы для вас.


## AngularJS Controller Sub-Generator

Sub-generator AngularJS Controller создаст новый контроллер AngularJS в папке **controllers** модуля. Чтобы создать новый контроллер AngularJS, снова запустите *slush meanjs* с помощью этой команды:

```
$ slush meanjs:angular-controller <controller-name>
```

Sub-generator запросит у вас имя модуля, под которым вы хотели бы создать новый контроллер, и создаст новый файл контроллера AngularJS в этой папке **controllers** модуля и тестовый файл в **tests** папки.

**Не забывайте!** На этот раз вы передаете имя контроллера в качестве аргумента.

## AngularJS View Sub-Generator

Как только у вас есть готовый файл контроллера, вы можете захотеть добавить представление, которое использует этот контроллер. Sub-generator представлений AngularJS создаст новое представление AngularJS в папке **views** указанного модуля и позволит вам добавить для него определение маршрута. Для создания нового представления AngularJS вам необходимо выполнить эту команду:

```
$ slush meanjs:angular-view <view-name>
```

Sub-generator запросит у вас имя модуля, под которым вы хотели бы создать новый вид, и некоторую дополнительную информацию о маршрутизации. Затем он создаст новый файл представления в папке **views** этого модуля и добавит состояние маршрутизации к файлу модуля **rout.js**. Если он не может найти файл маршрутов модуля, он создаст его для вас.


## AngularJS Service Sub-Generator

Sub-generator службы AngularJS создаст новую службу AngularJS в папке **services** указанного модуля. Чтобы создать новый сервис AngularJS, вам нужно выполнить эту команду:

```
$ slush meanjs:angular-service <service-name>
```

Sub-generator запросит у вас имя модуля, под которым вы хотите создать новую службу, и создаст новый файл службы AngularJS в папке **services** этого модуля.

## AngularJS Directive Sub-Generator

Sub-generator директивы AngularJS создаст новую директиву AngularJS в папке **directives**. Создание новой директивы AngularJS уже должно выглядеть знакомо:

```
$ slush meanjs:angular-directive <directive-name>
```

Sub-generator запросит у вас имя модуля, под которым вы хотели бы создать новую директиву, и создаст новый файл директивы AngularJS в папке **directives**.

## AngularJS Filter Sub-Generator

Генератор фильтров AngularJS создаст новый фильтр AngularJS в папке **filters** указанного модуля. Чтобы создать новый фильтр AngularJS, вам нужно снова вызвать *slush meanjs*:

```
$ slush meanjs:angular-filter <filter-name>
```

Sub-generator запросит у вас имя модуля, под которым вы хотите создать новый фильтр, и создаст новый файл фильтра AngularJS в папке этого модуля **filters**.


## AngularJS Config Sub-Generator


Конфигурационный sub-generator AngularJS создаст новый раздел конфигурации AngularJS в папке **config** указанного модуля. Чтобы создать новый конфигурационный файл AngularJS, просто вызовите *slush meanjs*:
```
$ slush meanjs:angular-config <config-name>
```

Sub-generator запросит у вас имя модуля, под которым вы хотите создать новую конфигурацию, и создаст новый файл конфигурации AngularJS в папке **config** этого модуля.

## AngularJS Test Sub-Generator

Ваше MEAN-приложение поставляется с предустановленным тестером Karma и средой тестирования Jasmine. Для тестирования ваших контроллеров AngularJS вам необходимо создать тестовый файл, который Karma позже будет использовать для запуска тестов. Для этого мы предоставили вам тестовый sub-generator AngularJS. Создать новый тест AngularJS легко, просто выполните эту команду:

```
$ slush meanjs:angular-test <controller-name>
```

Это создаст тестовый файл для вашего контроллера, и если sub-generator не найдет указанный файл контроллера, он создаст его для вас.


**Не забывайте!** Вы должны передать имя контроллера в качестве аргумента.

## Express Model Sub-Generator

Часто вы обнаружите необходимость просто создать одну модель Express. Sub-generator моделей Express поможет вам создать модель Express в папке **app / models**. Для создания новой модели просто используйте *slush meanjs*:

```
$ slush meanjs:express-model <model-name>
```

Это создаст новую пустую модель в папке **app / models** и тестовый файл в папке **app / tests**.


**Примечание:** Рекомендуется не называть свою модель во множественном числе и использовать вместо нее форму единственного числа. то есть статья, а не статьи

## Express Controller Sub-Generator

Еще одна повторяющаяся задача - создание пустого контроллера Express. Sub-generator контроллера Express поможет вам создать контроллер Express в папке **app / controllers**. Для создания нового контроллера просто используйте *slush meanjs*:

```
$ slush meanjs:express-controller <controller-name>
```

Это создаст новый пустой контроллер в папке **app / controllers**.

## Express Routes Sub-Generator

Для отправки HTTP-запросов к методам вашего контроллера вам потребуется использовать файл маршрутизации в папке **app / rout**. Sub-generator экспресс-маршрутов поможет вам добавить новый пустой файл маршрутов. Чтобы создать новый файл маршрутов, выполните команду *slush meanjs*:

```
$ slush meanjs:express-route <route-name>
```

Это создаст новый пустой файл маршрута в папке **app / routes**.

## Express Test Sub-Generator

Ваше MEAN-приложение поставляется в комплекте с инфраструктурой тестирования Mocha. Чтобы протестировать ваши модели Express, вам нужно создать новый тестовый файл, который Mocha будет использовать при выполнении тестов. Для этого мы предоставили вам тестовый sub-generator Express. Создать новый экспресс-тест очень просто, просто выполните эту команду:

```
$ slush meanjs:express-test <model-name>
```

Это создаст тестовый файл для вашей модели Express, и если sub-generator не найдет указанную модель, он создаст его для вас.


**Не забывайте!** Вы должны передать имя модели в качестве аргумента.

## Знакомство со Slush

Slush - это инструмент, который использует Gulp для строительных проектов.

Slush не содержит ничего «из коробки», кроме возможности найти установленные генераторы Slush и запускать их с отрывом.

Чтобы узнать больше о Slush, ознакомьтесь с [documentation] (https://github.com/klei/slush).

## Contributing

See the [CONTRIBUTING Guidelines](https://github.com/arvindr21/slush-meanjs/blob/master/CONTRIBUTING.md)

## Support
Если у вас есть какие-либо проблемы или предложения, пожалуйста, откройте вопрос [here](https://github.com/arvindr21/slush-meanjs/issues).

## License

Лицензия MIT

Copyright (c) 2014, Arvind Ravulavaru

Таким образом, разрешение предоставляется бесплатно любому лицу
получение копии этого программного обеспечения и сопутствующей документации файлы («Программное обеспечение»), чтобы иметь дело с Программным обеспечением без ограничение, включая, помимо прочего, права на использование, копировать, изменять, объединять, публиковать, распространять, сублицензировать и / или продавать копии Программного обеспечения и разрешать лицам, которым Программное обеспечение предоставляется для этого при условии следующего условия:

Вышеуказанное уведомление об авторских правах и это разрешение должно быть включены во все копии или существенные части Программного обеспечения.

ПРОГРАММНОЕ ОБЕСПЕЧЕНИЕ ПРЕДОСТАВЛЯЕТСЯ «КАК ЕСТЬ», БЕЗ КАКИХ-ЛИБО ГАРАНТИЙ, ЯВНЫЕ ИЛИ ПОДРАЗУМЕВАЕМЫЕ, ВКЛЮЧАЯ, НО НЕ ОГРАНИЧЕННЫЕ ГАРАНТИИ ИЗДЕЛИЯ, ПРИГОДНОСТИ ДЛЯ ОСОБЫХ ЦЕЛЕЙ И
НЕПОСЯГАТЕЛЬСТВА. НИ В КОЕМ СЛУЧАЕ НЕ ДОЛЖНЫ АВТОРЫ ИЛИ АВТОРСКИЕ ПРАВА
Держатели несут ответственность за любые претензии, ущерб или другую ответственность, В ДЕЙСТВИИ ДЕЙСТВИЯ ДОГОВОРА, ИСПЫТАНИЯ ИЛИ ИНОГО
ОТ, ИЗ ИЛИ В СВЯЗИ С ПРОГРАММНЫМ ОБЕСПЕЧЕНИЕМ ИЛИ ИСПОЛЬЗОВАНИЕМ
ДРУГИЕ СДЕЛКИ В ПРОГРАММНОМ ОБЕСПЕЧЕНИИ.
