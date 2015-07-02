The General Guidelines section provides detailed discussion of the design and ideas behind the plugin, explaining why certain things are as they are. It covers the features in more detail than the API documentation, which just briefly explains the various methods and options available.

If you've decided to use the validation plugin in your application and want to get to know it better, it is recommended that you read the guidelines.

### Fields with complex names (brackets, dots)

When you have a name attribute like user[name], make sure to put the name in quotes. More details in the [General Guidelines](http://jqueryvalidation.org/reference).

### Too much recursion

Another common problem occurs with this code:

```javascript
$("#myform").validate({
  submitHandler: function(form) {
    // some other code
    // maybe disabling submit button
    // then:
    $(form).submit();
  }
});
```

This results in a too-much-recursion error: $(form).submit() triggers another round of validation, resulting in another call to submitHandler, and voila, recursion. Replace that with form.submit(), which triggers the native submit event instead and not the validation.

So the correct code looks slightly different:

```javascript
$("#myform").validate({
  submitHandler: function(form) {
    form.submit();
  }
});
```

### Demos

The Marketo sign-up form, [step 1](http://jqueryvalidation.org/files/demo/marketo/)  
The Marketo sign-up form, [step 2](http://jqueryvalidation.org/files/demo/marketo/step2.htm)

Based on an old version of the marketo.com sign-up form. The custom validation was once replaced with this plugin. Thanks to Glen Lipka for contributing it!

_Notable features of the demo_:

Customized message display: No messages displayed for the required method, only for typing-errors (like wrong email format); A summary is displayed at the top ("You missed 12 fields. They have been highlighted below.")
Remote validation of email field. Try to enter eg. glen@marketo.com
Integration with masked-input plugin, see Zip and Phone fields and Credit Card Number on step 2
A custom method for making the billing address on step 2 optional when "Same as Company Address" is checked
A custom method for checking the password: Checks that the password contains at least one number and one character and that it is at least 6 characters long. If the user blurs the field with an invalid value, the input is emptied and gets focus again.