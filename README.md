# jQuery UI Monthpicker

![Pick a month](https://github.com/tlemens/jquery-ui-monthpicker/blob/master/monthpicker.gif)

## HTML

```html
<input class="js-monthpicker" type="hidden"><input type="text">
```

Field | Value
--- | ---
Hidden | Actual date (1th of the picked month)
Text | Picked month

## jQuery

```js
$('.js-monthpicker').monthpicker();
```

You may want to [customize the format](http://api.jqueryui.com/datepicker/#utility-formatDate):

```js
$('.js-monthpicker').monthpicker({ altFormat: 'MM y' });
```

## Style

Use the ui-monthpicker class for styling.

```css
.ui-monthpicker {
  margin-top: 18px;
}
.ui-monthpicker .ui-datepicker-month {
  display: none;
}
.ui-monthpicker td span {
  padding: 5px;
  cursor: pointer;
  text-align: center;
}
```
## Dependencies

[jQuery UI Datepicker](https://github.com/jquery/jquery-ui)

## License

[MIT](http://clemenst.mit-license.org)
