# За что я не люблю комментарии

## Ни к одному комментарию нет доверия

Для начала небольшая логическая цепочка:

* Аксиома: _все_ люди несовершенны, нет _ни одного_ идеального. Т.е. все люди совершают ошибки. В зависимости от человека или ситуации ошибок может быть больше или меньше, они могут быть мелкие или серьёзные, но они есть _всегда_.  
Если читатель поставит это утверждение под сомнение – покиньте мою территорию, с неадекватами мне обсуждать нечего.
* Отсюда следует вывод: _любой_ процесс, который (весь или некоторые его этапы) опирается на действия человеков, будет хотя бы иногда сбоить.  
(Маленькое лирическое отступление: из вышесказанного следует, что все процессы желательно максимально автоматизировать.)
* Процесс "Работа с комментариями" включает такой пункт: "В случае изменения кода разработчик должен актуализировать соответствующие комментарии". Из вышесказанного следует, что это будет происходить не всегда. А значит, будут появляться комментарии, которые _врут_.
* Если любой комментарий в коде может оказаться ложью, и нет надёжного способа сразу отличить истинные комментарии от ложных, то что мне, как читателю, делать? Есть два пути: первый – каждый нужный в данный момент комментарий валидировать, т.е. определять его истинность или ложность – а это безумно большие затраты ресурсов. Второй – не верить ни одному и, соответственно, все игнорировать.  
Если читатель верит _всем_ комментариям в коде – покиньте мою территорию, настолько наивным людям я вряд ли смогу что-либо донести.
* А если я всё равно игнорирую все комментарии, то пользы от них – ноль, а вот вред есть: они замусоривают код и мешают его чтению. А значит, их писать не просто бесполезно, а **вредно**.

«_Код никогда не лжет, а вот с комментариями такое случается_» — [Рон Джеффрис](https://ru.qaz.wiki/wiki/Ron_Jeffries)

## "Комментарии облегчают понимание кода" (C)

Да, конечно. Только вот при чтении кода коментарии [чаще мешают, чем помогают](./two_types_of_read.md) (авторство моё).

## Комментарии нарушают DRY

См. [здесь](./DRY_misunderstanding.md) моё мнение.

А вот [комментарий с Хабра](https://habr.com/ru/company/piter/blog/460725/#comment_20413345): "_Комментарии, не к публичному API, а по месту — это злое зло, препятствующее рефакторингу и нарушающее принцип DRY второго рода_".

И в [этой статье](https://habr.com/ru/company/productivity_inside/blog/493288/) про то же в п.4.

## Комментарии – костыль, прикрывающий непрофессионализм

Очень часто разработчик не умеет в нейминг и декомпозицию, и из-за этого его код непонятен. Конечно, в этой ситуации тянет сделать код более понятным с помощью комментариев.

Но очевидно, что это – костыль. Надо прокачивать в себе скиллы нейминга и декомпозиции, а не прятаться за комменты.

Полностью согласен [с товарищем с Хабра](https://habr.com/ru/company/piter/blog/460725/#comment_20413121): "_Краткие и лаконичные — это как раз о искусстве именования сущностей. И да, если не умеете — оправдываетесь в комментах_".

## Лучше тратить время/силы на другое

Комментарии ещё нужно уметь писать. Зачастую они
* контекстнозависимые  
Вот здесь [примеры из моей практики](./comments_examples.md).

* их слишком много  
И опять [цитата с Хабра](https://habr.com/ru/company/alconost/blog/443678/): "_Когда код перегружен неактуальными комментариями, последние скорее всего будут игнорироваться_".

* просто непонятные.

Значит, надо (а) обучать программистов писать правильные комментарии, (б) на код-ревью отслеживать, чтобы не было кривых комментов, а значит и (в) писать регламенты на комментирование.

Овердофига трат ресурсов, хотя можно просто взять и отменить комменты вообще. Да, в этом случае придётся всё тоже самое (обучать, контролировать, регламентировать) делать в отношении других навыков – нейминга и декомпозиции, но эти скиллы качать надо в любом случае.

---

И на прощание длинная цитата – расслабьтесь, эта не с Хабра 😆, это Peter Sommerlad:  
"**_Только Код Скажет Правду_**

_Конечная семантика программы определяется исходным кодом. Если он только в двоичной форме, его будет трудно прочитать. Но, если это ваша программа, любая коммерческая разработка ПО, проект с открытым исходным кодом или код на динамически интерпретируемом языке, тогда исходный код программы доступен. Когда вы смотрите на исходный код, смысл программы должен быть очевиден. Чтобы узнать, что делает программа, исходный код – вот всё, в чём вы можете быть уверены. Даже самый точный документ с ТЗ не говорит всей правды: он содержит только высокоуровневые намерения, а не подробное описание того, что делает программа. Проектный документ может отражать запланированный дизайн, но в нём не будет необходимых деталей реализации. Кроме того, такие документы могут устаревать и больше не отражать текущую реализацию. Также они могут быть утеряны … или их вообще никогда не писали. Исходный код – единственное, что у вас осталось._

_Имея это в виду, спросите себя, насколько чётко ваш код сообщает вам или любому другому программисту, что он делает._

_Вы можете подумать, что комментарии расскажут всё, что вам нужно знать. Но имейте в виду, что комментарии - это не исполняемый код. Они могут быть такими же ошибочными, как и другие формы документации. Существует убеждение, что комментарии - это всегда хорошо, поэтому некоторые программисты постоянно пишут огромное количество комментариев, даже переформулируя и объясняя мелочи, уже очевидные из кода. Это неправильный способ объяснения работы вашего кода._

_Если вашему коду нужны комментарии, подумайте о его рефакторинге, чтобы этого не требовалось. Длинные комментарии могут загромождать пространство на экране и даже могут автоматически скрываться вашей IDE. Если вам нужно объяснить изменение, сделайте это в комментарии коммита системы контроля версий, а не в коде._

_Что вы можете сделать, чтобы ваш код действительно выражал ваши намерения как можно яснее? Стремитесь использовать хорошие имена. Структурируйте свой код с учетом целостной функциональности (одна задача – один класс, одна функция – один метод), что также упрощает именование. Разделите свой код для достижения ортогональности (повторного использования). Напишите автоматизированные тесты, объясняющие предполагаемое поведение, и проверьте интерфейсы. Безжалостно проводите рефакторинг, когда вы находите более простое решение. Сделайте свой код максимально простым для чтения и понимания._

_Относитесь к своему коду как к любому другому произведению, например к стихотворению, эссе, публичному блогу или важному электронному письму. Тщательно обдумывайте то, что вы пишете, чтобы оно делало то, что должно, и как можно более чётко выражало то, что делает. Чтобы произведение продолжало выражать ваши намерения даже вашим потомкам. Помните, что полезный код используется намного дольше, чем изначально предполагалось. Обслуживающие его программисты будут вам благодарны._".

---

_Дедушка Волшебник, 2021-03-14_