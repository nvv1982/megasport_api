#Описание API (Спецификация REST Service)

<p>Вместо <b>localhost:3000</b> нужно указать реальный IP адрес и порт </p>
<hr>
<h2>Работа с заказами (Шапка)</h2>

<h4>Методы</h4>
<ul> 
<li> Получить список заказов (GET) url: http://localhost:3000/orders.json </li>
<li> Получить  заказо со строками (GET) url: http://localhost:3000/orders/[id].json </li>
<li> Добавить заказ (POST) с параметрами url: http://localhost:3000/orders.json </li>
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
	"refpost": "s12",
	"orderrows": [
		{
			"art": "ANT000001",
			"cnt": 1,
			"sizes": "XS",
			"price": 200,
			"model": "M1",
			"section": "S1",
			"brand": "ANTA",
			"img_url": "https://www.google.com.ua/search?sourceid=chrome-psyapi2&ion=1",
			"disc": 10.10
		}
		]
}
</code>

<h4>Описение полей</h4>
<ul>
	<li>ordid: Номер заказа с сайта (не обязательно)</li>
	<li>name: Имя клиента</li>
	<li>surrname: Фамилия клиента</li>
	<li>complete: Статус выполнения заказа</li>
	<li>totalprice: Сумма заказа 00.00</li>
	<li>phone: Телефон</li>
	<li>card: Номер ДК</li>
	<li>paid: Флаг оплаты</li>
	<li>dat: Дата DD.MM.YYYY HH:MI:SS</li>
	<li>descr: Описание</li>
	<li>err: Ошибка (не обязательно)</li>
	<li>bonus_in: Начисленные бонусы (не обязательно) </li>
	<li>bonus_out: Списанные бонусы (не обязательно)</li>
	<li>email: e-mail</li>
	<li>refcity: ID из API НП</li>
	<li>refpost: ID из API НП</li>	
</ul>

<h2>Работа с заказами (строки)</h2>

<h4>Методы</h4>
<ul> 
<li> Добавить строку заказа (POST) с параметрами url: http://localhost:3000/orderrows.json </li>
<li> Обновить строку заказа (PUT) с параметрами url: http://localhost:3000/orderrows/[id].json </li>
<li> Удалить строку зака (DELETE)  url: http://localhost:3000/orderrows/[id].json 
</ul>
 
<h4>Параметры orderrows.json</h4>
<p>Параметры передаются в теле сообщения в формате JSON </p>
<code>
{
	"ordid": 10,
	"art": "ANT000001",
	"cnt": 1,
	"sizes": "XL",
	"price": 400.0,
	"model": "Кепка",
	"section": "1",
	"brand": "ANTA",
	"img_url": "http://a.jpg",
	"disc": 100.0,
	"err": "",
	"bonus_disc": 100.0,
	"act_disc": 0.0
}
</code>

<h4>Описение полей</h4>
<ul>
	<li>ordid: ID заказа (из базы). Внимание !!! не путать с номером заказа !</li>
	<li>art:  Артикул товара</li>
	<li>cnt: Количество</li>
	<li>sizes: Размер</li>
	<li>price: <b>Цена к оплате  00.00 </b></li>
	<li>model: Модель</li>
	<li>section: Секция</li>
	<li>brand: Бренд</li>
	<li>img_url: ссылка на товар</li>
	<li>disc: Общая Скидка по ДК</li>
	<li>bonus_disc: Общая Скидка по бонусам </li>
	<li>act_disc: Общая скидка Скидка по акциям </li>
	<li>err: Ошибка (не обязательно)</li>
</ul>
