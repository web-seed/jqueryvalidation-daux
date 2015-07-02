### Downloading the prebuilt files

Prebuilt files can be downloaded from [here](http://jqueryvalidation.org/files/jquery-validation-1.13.1.zip).

### Downloading the latest changes

The unreleased development files can be obtained by:

1. [Downloading](https://github.com/jzaefferer/jquery-validation/archive/master.zip) or [Forking](https://github.com/jzaefferer/jquery-validation) this repository
2. [Setup the build](https://github.com/jzaefferer/jquery-validation/blob/master/CONTRIBUTING.md#build-setup)
3. Run `grunt` to create the built files in the "dist" directory

### Including it on your page

Include jQuery and the plugin on a page. Then select a form to validate and call the validate method.

```
<form>
    <input required>
</form>
<script src="jquery.js"></script>
<script src="jquery.validate.js"></script>
<script>
	$("form").validate();
</script>
```
Alternatively include jQuery and the plugin via requirejs in your module.

``` 
define(["jquery", "jquery.validate"], function( $ ) {
    $("form").validate();
});
```
For more information on how to setup a rules and customizations, [check the documentation](http://jqueryvalidation.org/documentation/).


## Reporting issues and contributing code

See the [Contributing Guidelines](https://github.com/jzaefferer/jquery-validation/blob/master/CONTRIBUTING.md) for details.

**IMPORTANT NOTE ABOUT EMAIL VALIDATION.** As of version 1.12.0 this plugin is using the same regular expression that the [HTML5 specification suggests for browsers to use](https://html.spec.whatwg.org/multipage/forms.html#valid-e-mail-address). We will follow their lead and use the same check. If you think the specification is wrong, please report the issue to them. If you have different requirements, consider [using a custom method](http://jqueryvalidation.org/jQuery.validator.addMethod/).

## License

Copyright © Jörn Zaefferer
Licensed under the MIT license.



