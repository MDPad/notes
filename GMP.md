---
Theme:
  - "[[Go]]"
---
Design doc - https://golang.org/s/go11sched

Модель исполнения goroutines в рантайме Go: **Goroutine–Machine-Processor**

| Компонент | Название              | Что это                                  |
| --------- | --------------------- | ---------------------------------------- |
| **G**     | Goroutine             | Лёгкий поток исполнения (ваша функция)   |
| **M**     | Machine (OS thread)   | Поток ОС, исполняющий goroutines         |
| **P**     | Processor (вирт. CPU) | Планировщик + очередь задач (goroutines) |

| Файл                  | Описание                                             | Ссылка |
|-----------------------|------------------------------------------------------|--------|
| `runtime/proc.go`     | Основной код планировщика (создание/переключение G/M/P) | [GitHub](https://github.com/golang/go/blob/master/src/runtime/proc.go) |
| `runtime/sched.go`    | Очереди, `runq`, обработка планирования              | [GitHub (внутри proc.go)](https://github.com/golang/go/blob/master/src/runtime/proc.go#L400) |
| `runtime/runtime2.go` | Типы `G`, `M`, `P`, флаги и статусы                  | [GitHub](https://github.com/golang/go/blob/master/src/runtime/runtime2.go) |
| `runtime/preempt.go`  | Механизмы preemption (с Go 1.14+)                    | [GitHub](https://github.com/golang/go/blob/master/src/runtime/preempt.go) |
| `runtime/mgc.go`      | Интеграция сборщика мусора с планировщиком          | [GitHub](https://github.com/golang/go/blob/master/src/runtime/mgc.go) |
