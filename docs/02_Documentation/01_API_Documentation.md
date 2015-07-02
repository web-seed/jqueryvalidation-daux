You're probably looking for

**Options for the [validate()](http://jqueryvalidation.org/validate) method**

If not, read on.

Throughout the documentation, two terms are used very often, so it's important that you know their meaning in the context of the validation plugin:

* **method:** A validation method implements the logic to validate an element, like an email method that checks for the right format of a text input's value. A set of standard methods is available, and it is easy to write your own.
* **rule:** A validation rule associates an element with a validation method, like "validate input with name "primary-mail" with methods "required" and "email".

### Plugin methods

This library adds three jQuery plugin methods, the main entry point being the validate method:

* [validate()](http://jqueryvalidation.org/validate) – Validates the selected form.
* [valid()](http://jqueryvalidation.org/valid) – Checks whether the selected form or selected elements are valid.
* [rules()](http://jqueryvalidation.org/rules) – Read, add and remove rules for an element.

### Custom selectors

This library also extends jQuery with three custom selectors:

* [:blank](http://jqueryvalidation.org/blank-selector) – Selects all elements with a blank value.
* [:filled](http://jqueryvalidation.org/filled-selector) – Selects all elements with a filled value.
* [:unchecked](http://jqueryvalidation.org/unchecked-selector) – Selects all elements that are unchecked.

### Validator

The validate method returns a Validator object that has a few public methods that you can use to trigger validation programmatically or change the contents of the form. The validator object has more methods, but only those documented here are intended for usage.

* [Validator.form()](http://jqueryvalidation.org/Validator.form) – Validates the form.
* [Validator.element()](http://jqueryvalidation.org/Validator.element) – Validates a single element.
* [Validator.resetForm()](http://jqueryvalidation.org/Validator.resetForm) – Resets the controlled form.
* [Validator.showErrors()](http://jqueryvalidation.org/Validator.showErrors) – Show the specified messages.
* [Validator.numberOfInvalids()](http://jqueryvalidation.org/Validator.numberOfInvalids) – Returns the number of invalid fields.

There are a few static methods on the validator object:

* [jQuery.validator.addMethod()](http://jqueryvalidation.org/jQuery.validator.addMethod) – Add a custom validation method.
* [jQuery.validator.format()](http://jqueryvalidation.org/jQuery.validator.format) – Replaces {n} placeholders with arguments.
* [jQuery.validator.setDefaults()](http://jqueryvalidation.org/jQuery.validator.setDefaults) – Modify default settings for validation.
* [jQuery.validator.addClassRules()](http://jqueryvalidation.org/jQuery.validator.addClassRules) – Add a compound class method.

### List of built-in Validation methods

A set of standard validation methods is provided:

* [required](http://jqueryvalidation.org/required-method) – Makes the element required.
* [remote](http://jqueryvalidation.org/remote-method) – Requests a resource to check the element for validity.
* [minlength](http://jqueryvalidation.org/minlength-method) – Makes the element require a given minimum length.
* [maxlength](http://jqueryvalidation.org/maxlength-method) – Makes the element require a given maxmimum length.
* [rangelength](http://jqueryvalidation.org/rangelength-method) – Makes the element require a given value range.
* [min](http://jqueryvalidation.org/min-method) – Makes the element require a given minimum.
* [max](http://jqueryvalidation.org/max-method) – Makes the element require a given maximum.
* [range](http://jqueryvalidation.org/range-method) – Makes the element require a given value range.
* [email](http://jqueryvalidation.org/email-method) – Makes the element require a valid email
* [url](http://jqueryvalidation.org/url-method) – Makes the element require a valid url
* [date](http://jqueryvalidation.org/date-method) – Makes the element require a date.
* [dateISO](http://jqueryvalidation.org/dateISO-method) – Makes the element require an ISO date.
* [number](http://jqueryvalidation.org/number-method) – Makes the element require a decimal number.
* [digits](http://jqueryvalidation.org/digits-method) – Makes the element require digits only.
* [creditcard](http://jqueryvalidation.org/creditcard-method) – Makes the element require a credit card number.
* [equalTo](http://jqueryvalidation.org/equalTo-method) – Requires the element to be the same as another one

Some more methods are provided as add-ons, and are currently included in additional-methods.js in the download package. Not all of them are documented here:

* [accept](http://jqueryvalidation.org/accept-method) – Makes a file upload accept only specified mime-types.
* [extension](http://jqueryvalidation.org/extension-method) – Makes the element require a certain file extension.
* [phoneUS](http://jqueryvalidation.org/phoneUS-method) – Validate for valid US phone number.
* [require_from_group](http://jqueryvalidation.org/require_from_group-method) – Ensures a given number of fields in a group are complete.


