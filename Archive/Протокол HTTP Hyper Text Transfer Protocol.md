202205071137
Tags: #компьютерные_сети

---

# Протокол HTTP Hyper Text Transfer Protocol
Находится на [[Прикладной уровень модели TCP-IP]]

Использует [[Протокол TCP Transmission Controll Protocol]]

Работает в режиме запрос-ответ 

Структура пакета HTTP:
- Запрос
	GET /courses/networks
- Статус ответа
	200 OK
- Заголовки
	Host: www.example.com (обязательно в HTTP 1.1)
	Content-Type: text/html; charset=UTF-8
- Тело сообщения
	Страница HTML
	
Методы:
- GET
- POST

Статусы:
![[Pasted image 20220507114552.png]]

Загрузка нескольких ресурсов:
![[Pasted image 20220507115430.png]]
Для загрузки каждого ресура  открывается новое TCP соединение. 

### Постоянное соединение HTTP keep-alive
- Не нужно каждый раз проходить процедуру трехкратного рукапожатия. 
- Нет необходимости каждый раз начинать передачу данных с маленьким размером окна TCP (медленный старт)
Необходимо добавить заголовок Connection: keep-alive

---
## Links