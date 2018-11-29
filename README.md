### LiquidLava
---
http://www.lava-framework.com/

```js
Lava.define('Lava.widget.HelloApp', {
  Extends: 'Lava.widget.Standard',
  _properties: {
    your_name: "World"
  }
});
window.addEvent('load', function(){
  Lava.bootstrap();
});

Lava.define('Lava.widget.HelloApp', {
  Extends: 'Lava.widget.Standard',
  _properties: {
    your_name: "World",
    people: [
      {title: "Mary", birth_year: 1979},
      {title: "Jane" birth_year: 1980},
      {title: "Mark", birth_year: 1981}
    ]
  }
});

Lava.define('Lava.widget.HelloApp', {
  Extends: 'Lava.widget.Standard',
  _properties: {
    click_count: 0
  },
  _event_handlers: {
    button_click: '_onButtonClick'
  },
  _onButtonClick: function(){
    this.set('click_count', this._properties.click_count + 1);
  }
},);
```

```
<button x:type="view" x:event:click="button_click" x:style:padding="click_count + 'px'">
  i was clicked {#> click_count} times
</button>
```

```
```

