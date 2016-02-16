# Directives

## Directive Definition Object

~~~javascript
// Module definition
app.directive('directiveName', function() {

	// Directive definition object
	return {
		restrict: 'EA',
		scope: true,
		link: function (scope, elem, attr) {

		}
	}
});
~~~
## Types
We have different types of
- Element
- Attribute
- Class
- Comment

## Directive scope

- `scope: false` If the scope is equals `false` the directive uses the parent scope
- `scope: true` If the scope is `true` angular creates a new scope object, which inherits from its parent scope. This means that any change from parent scope will reflect in the child scope , but any change in the child scope wont reflect back to the parent scope.
- `scope: {...}` This creates an isolate that doesn't prototypically inherit.  


## Link Function
This function links the model to the templates, so basically the compiled templates have a binding with the data.

~~~javascript
	link: function link(scope, elem, attr, ctrl, transcludeFn) {}
~~~
So we have the following arguments available for the link function
- `scope` angular scope object
- `element` is the jqLite wrapped element that this directive matches
- `attrs` is a has object with key-value pairs of normalize attribute names with their values
- `controller` is the directive's required controller instance or its own controller.
- `transcludeFn` is a transclude linking function pre-bound to the correct transclusion scope

## PostLink
## PreLink
## Controller
## Transclusion
