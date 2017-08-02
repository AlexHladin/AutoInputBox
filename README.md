# AutoInputBox
Auto input complete plugin with jQuery.

### Install
jQuery and jQuery.textchange is required, so include it first.
Include the script in your HTML file:

<script src="../auto_inputbox.js"></script>

### Usage
		$('#user-input').autoInput({
			url: 'https://jsonplaceholder.typicode.com/users',
			options
		});
		
Where 'options' is an optional parameter.

### Options
The default `options` are:
		{
			className: 'autoInput',
			formatElement: function(el) {
				return JSON.stringify(el).substring(20);
			},
			onItemSelected: function(el) {
				return $(el).html();
			},
			slideDownComplete: function() {
			}
		}
		
Where
- `className` - name of css classes prefix
- `formatElement` - function that map elements
- `onItemSelected` - function that return value that will be stored in input tag and submited
- `slideDownComplete` - function for actions on `slide complete`