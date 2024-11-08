# Документирование – надо ли?

Надо ли документировать разработку? Вопрос не бесспорный.

С одной стороны, документация – отличный способ шаринга информации. С другой – документация начинает устаревать с момента своего создания, и, когда вы изучаете какой-то документ, с вероятностью чуть менее 100% он уже не актуален.

Всё-таки, писать документацию скорее надо, чем нет. Вот мысли по этому поводу:

1. Даже в устаревших доках есть знания, которые могут быть полезны для новичка в теме. Главное для него – не забывать, что любая информация в документе может быть уже не верна 😃.
2. Иногда даже сам процесс написания доков имеет ценность, независимо от того, как вы поступите с результатом (например, сразу отправите в Корзину). Например, вам надо организовать процесс передачи экспертизы от одного сотрудника к другому (один увольняется, другой приходит ему на замену). В этом случае стоит назначить получателя экспертизы на роль техписа – его задача через интервью извлекать информацию из источника этой экспертизы и помещать её в документ.
3. Чем о более высокоуровневых концепциях идёт речь, тем медленнее они меняются. Поэтому писать доки на высокоуровневые вещи имеет больше смысла, чем на низкоуровневые. Например, описание архитектуры всей системы будет меняться достаточно редко.

И пара приёмов по поддержанию актуальности документации (дисклеймер: полностью они проблему, конечно, не решают, но позволяют притормозить процесс устаревания):

1. Назначьте на _каждый_ документ овнера (ответственного). Возможно, некоторые из них иногда 😆 будут свои документы актуализировать.
2. Используйте новичков в качестве тестировщиков документов. Про онбординге на новичка возлагается обязанность фиксировать все несоответствия между документами и реальностью, а также сообщать о них. Тут же надо организовать актуализацию документов по этим замечаниям (кто будет этим заниматься – вопрос технический, может быть овнер, может быть сам новичок, если овнеров нет, и т.д.).

---

_Дедушка Волшебник, 2021-12-22_