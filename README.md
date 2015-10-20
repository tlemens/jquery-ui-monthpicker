# jQuery UI Monthpicker
[![License](https://img.shields.io/npm/l/express.svg?style=flat)](http://clemenst.mit-license.org)

Pick a month.

![Pick a month](https://github.com/tlemens/jquery-ui-monthpicker/blob/master/monthpicker.gif)


## HTML

```html
<input class="js-monthpicker" type="hidden"><input type="text">
```

--- | ---
Hidden field: | Actual date (1th of the picked month)
Text field: | Month

## jQuery

```js
$('.js-monthpicker').monthpicker();
```

You may want to [customize the format](http://api.jqueryui.com/datepicker/#utility-formatDate):

```js
$('.js-monthpicker').monthpicker({ altFormat: 'MM y' });
```

## Style

Use the ui-monthpicker class to style the monthpicker.

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











[customize the format](http://api.jqueryui.com/datepicker/#utility-formatDate)

Use the altField option to customize the month format.

business_hour = BusinessHour.new(opening: '9:00', closing: '17:00')
business_hour.opening
 => 32400
business_hour.closing
 => 61200

To convert back to time of day:
```ruby
TimeOfDayAttr.l(business_hour.opening)
 => '9:00'
TimeOfDayAttr.l(business_hour.closing)
 => '17:00'
```

You could also omit minutes at full hour:
```ruby
TimeOfDayAttr.l(business_hour.opening, omit_minutes_at_full_hour: true)
 => '9'
```

### Formats

The standard formats for conversion are 'default' and 'hour'.
```yml
en:
  time_of_day:
    formats:
      default: '%k:%M'
      hour: '%k'
```

You can overwrite them or use custom formats:
```yml
en:
  time_of_day:
    formats:
      custom: '%H-%M'
```

Pass the formats you want for conversion:
```ruby
class BusinessHour < ActiveRecord::Base
  time_of_day_attr :opening, formats: [:custom]
end
```

```ruby
business_hour = BusinessHour.new(opening: '09-00')
business_hour.opening
 => 32400
TimeOfDayAttr.l(business_hour.opening, format: :custom)
 => '09-00'
```

### time of day field

To get a text field with the converted value:
```erb
<%= form_for(business_hour) do |f| %>
  <%= f.time_of_day_field(:opening) %>
<% end %>
```

## License

[MIT](http://clemenst.mit-license.org)

