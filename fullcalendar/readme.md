# FullCalendar JS

## init

```js
var calendar = new Calendar(calendarEl);
```


## Event нэмэх

JSON оор event датаг нэмэх нь энэ хэдэн аргууд байна



***


## event object structure

Ерөнхийдөө бол хамгийн энгийн нь
```json
{
    title : 'event1',
    start : '2010-01-01'
},
```

Энэ эхлэхээс дуусах огноо хүртэлх бүх өдөрлүү сунасан байдалтай харагдана.

```json
{
    title : 'event2',
    start : '2010-01-05',
    end   : '2010-01-07'
},

```

allDay нь идэвхигүй үед эхлэх огноо нь календар дээр харагдана
```json
{
      title  : 'event3',
      start  : '2010-01-09T12:30:00',
      allDay : false // will make the time show
}
```
`onClick` үйлдэл нэмэх хэрэгтэй бол 
```
events: [
    {
      title: 'My Event',
      start: '2010-01-01',
      url: 'https://google.com/'
    }
    // other events here
  ],
  eventClick: function(info) {
    info.jsEvent.preventDefault(); // don't let the browser navigate

    if (info.event.url) {
      window.open(info.event.url);
    }
  }
```
