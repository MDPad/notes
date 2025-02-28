---
Theme:
  - "[[Go]]"
---
1. **Основы язык Go**
	1. **Базовые типы, конструкции и библиотеки.**
		1. Типы string, rune, пакеты unicode, fmt, strconv, strings.
			*Примеры вопрос для проверки:*
			- [ ] *Что такое UTF-8? Какие его основные характеристики/особенности?* 
			- [ ] *Что из себя представляют строки в Go? Как перебирать символы строки?*
			- [ ] *Как отформатировать/преобразовать число в строку и обратно?*
			- [ ] *Как произвести поиск в строке?*
		2. Типы struct, array, slice, map, указатели, пакеты bytes, sort.
			*Примеры вопрос для проверки:*
			- [ ] *Если переменную одного из указанных выше типов передать в функцию и там ее модифицировать, то будет ли это изменение видно снаружи?*
			- [ ] *Как отсортировать slice?*
		3. Типы interface, error, конструкция type switch, пакет errors.
		   *Примеры вопрос для проверки:*
			- [ ] *Как узнать лежит ли в интерфейсе строка?*
			- [ ] *Как проверить ошибку на конкретный тип/значение?*
		4. Generics.
		   *Примеры вопрос для проверки:*
			- [ ] *В чем разница между реализации функции как generic и реализацией с передачей в нее интерфейсов?*
			- [ ] *Как реализовать тип с методом Increase(int)int, чтобы добавляемое число кастомизировалось с помощью generics?*
			- [ ] *Как сделать type switch для generic типа?*
		5. Пакет json.
		   *Примеры вопрос для проверки:*
			- [ ] *Как реализовать кастомную (де)сериализацию?*
			- [ ] *Зачем нужен RawMessage?*
		6. Context. 
		   *Примеры вопрос для проверки:*
			- [ ] *Какие две основные возможности дает context (для чего использовать Context)?*
			- [ ] *Можно ли передавать все параметры функции через контекст?*
		7. io.Reader/Writer, пакеты io, os. 
		   *Примеры вопрос для проверки:*
			- [ ] *Как прочитать файл?*
			- [ ] *Что такое io.Reader?*
		8. *Defer/Panic/Recover.*
		   *Примеры вопрос для проверки:*
			- [ ] *Когда вызывается defer.*
	2. Инструментарий Go.
		1. Форматирование кода
		2. Правильное написание комментариев (включая форматирование).
		3. Сборка с тегами.
		4. Кросcкомпиляция.
		5. go env.
	3. Go modules.
		*Примеры вопрос для проверки:*
		- [ ] *Как осуществляется версионирование модулей?*
		- [ ] *Как подключить модуль из репозитория, если он без тега?*
		- [ ] *Как выяснить почему конкретный модуль подтягивается при сборке?*
	4. Тестирование - пакет testing.
		*Примеры вопрос для проверки:*
		- [ ] *Как выполнить подготовку перед запуском тестов?*
		- [ ] *Как проверить уровень покрытия кода тестами?*
		- [ ] *Как логировать процесс выполнения тестов?*
	5. Linting (golangci-lint).
		*Примеры вопрос для проверки:*
		- [ ] *Зачем использовать линтер?*
		- [ ] *Что (примерно) умеет линтер отлавливать?*
		- [ ] *Как подключить и запустить линтер?*
	6. Асинхронщина и синхронизация.
		- [ ] *Goroutines*
		- [ ] *Каналы (select, range, close)*
		- [ ] *Пакет Sync*
		- [ ] *Пакет Atomic*
	7. Профилирование и отладка.
	8. Пакеты reflect & unsafe.
		1. +- reflect/unsafe.
		2. (можно ли получить доступ к приватным полям используя reflect или unsafe)
	9. Пакеты html/template & text/template.
	10. Пакет SQL.
	11. Кодогенерация.
2. Технологии и их использование в Go (зависит от потребностей команды)
	1. PostgreSQL + пакет sql.
	2. Redis.
	3. Clickhouse.
	4. GRPC

## Где черпать информацию

Тут все без изысков:
1. Go tour (для азов языка) - https://go.dev/tour
2. **Официальная спецификация языка** - https://go.dev/ref/spec
3. **Код библиотек** (в т.ч. стандартных)
4. **Блог Go (там бывают полезные статьи)** - https://go.dev/blog/
5. Effective Go - https://go.dev/doc/effective_go
6. Wikipedia - в основном по структурам и алгоритмам данных без углубления

Если невмоготу без книжек (сам не читал):
1. Программирование на Go. Разработка приложений XXI века (Марк Саммерфильд) - попроще
2. Golang для профи. Работа с сетью, многопоточность, структуры данных и машинное обучение с Go (Михалис Цукалос) - посложнее