#Описание API (Спецификация REST Service)

<p>Вместо <b>localhost:3000</b> нужно указать реальный IP адрес и порт </p>
<hr>
<p>Для работы с заказами url: http://localhost:3000/orders.json </p>
<ul> Методы
<li> Получить список заказов (GET)</li>
<li> Добавить заказ (POST) с параметрами </li>
<li> Обновить заказ (PUT) с параметрами url: http://localhost:3000/orders/[id].json </li>
<li> Удалить зака (DELETE)  url: http://localhost:3000/orders/[id].json 
</ul>
 
<h4>Параметры orders.json</h4>
<p>Параметры передаются в теле сообщения в формате JSON </p>
<code>
{
	"ordid": 10,
	"name": "Иван",
	"surrname": "Иванов",
	"complete": 0,
	"totalprice": 1000.0,
	"phone": "063000000",
	"card": "20000000000002",
	"paid": 1000,
	"dat": "01.12.2015 22:00:00",
	"descr": "Тестовый заказ",
	"err": "",
	"bonus_in": 1000,
	"bonus_out": 100,
	"email": "test@test.ua",
	"refcity": "s1",
	"refpost": "s12"
}
</code>