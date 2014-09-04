angular-jquery-autocomplete
===========================

jQuery UI autocomplete (http://jqueryui.com/autocomplete/) to AngularJS

### Scripts

```html
<script src="//code.jquery.com/jquery-2.1.1.min.js"></script>
<script src="//code.jquery.com/ui/1.11.0/jquery-ui.min.js"></script>
<script src="scripts/angular-jquery-autocomplete.js"></script>
```

### App

```js
var app = angular.module('YourApp', ['angular-jquery-autocomplete']);
```

### View

```html
<input id="LabelDevice" placeholder="{{ 'Events_Search' | translate }}" class=" form-control" data-ng-model="event.device.label" autocomplete autocompleteconfig="labelDeviceAutoComplete" />
```

### Controller

```js
$scope.labelDeviceAutoComplete = {
	source: function (request, response) {

		var array = [];

		array.push({ label: 'sss', value: 1 });

		response(array);
	},
	minLength: 3,
	select: function (event, ui) {
		this.value = ui.item.label;

		return false;
	}
};
```
