Automatically set the active class for the currently selected Bootstrap menu item
====

HTML
---
```
<ul class="nav nav-sidebar">
	<li active-class="active"><a href="#/Item1">Item1</a></li>
	<li active-class="active"><a href="#/Item2">Item2</a></li>
	...
</ul>
```

AngularJS directive
---
```
angular.module('AppName').directive('activeClass', [function() {
	return {
    	link: function(scope, element, attrs) {
			var anchorLink = element.find('a')[0].getAttribute('ng-href') || element.find('a')[0].getAttribute('href');
			anchorLink = anchorLink.replace(/^#/, '');
			scope.$on("$routeChangeSuccess", function (event, current) {
				if (current.$$route && current.$$route.originalPath.indexOf(anchorLink) === 0) {
					element.addClass(attrs.activeClass);
				}
				else {
					element.removeClass(attrs.activeClass);
				}
			});
		}
	};
}]);
```
