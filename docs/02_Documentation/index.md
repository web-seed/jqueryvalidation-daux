## Validate forms like you've never validated before!

**"But doesn't jQuery make it easy to write your own validation plugin?"**  
Sure, but there are still a lot of subtleties to take care of: You need a standard library of validation methods (such as emails, URLs, credit card numbers). You need to place error messages in the DOM and show and hide them when appropriate. You want to react to more than just a submit event, like keyup and blur.  
You may need different ways to specify validation rules according to the server-side enviroment you are using on different projects. And after all, you don't want to reinvent the wheel, do you?

**"But aren't there already a ton of validation plugins out there?"**  
Right, there are a lot of non-jQuery-based solutions (which you'd avoid since you found jQuery) and some jQuery-based solutions. This particular one is one of the oldest jQuery plugins (started in July 2006) and has proved itself in projects all around the world. There is also an [article](http://bassistance.de/2007/07/04/about-client-side-form-validation-and-frameworks/) discussing how this plugin fits the bill of the should-be validation solution.

Not convinced? Have a look at this [example](http://jqueryvalidation.org/files/demo/):

```
<form class="cmxform" id="commentForm" method="get" action="">
  <fieldset>
    <legend>Please provide your name, email address (won't be published) and a comment</legend>
    <p>
      <label for="cname">Name (required, at least 2 characters)</label>
      <input id="cname" name="name" minlength="2" type="text" required>
    </p>
    <p>
      <label for="cemail">E-Mail (required)</label>
      <input id="cemail" type="email" name="email" required>
    </p>
    <p>
      <label for="curl">URL (optional)</label>
      <input id="curl" type="url" name="url">
    </p>
    <p>
      <label for="ccomment">Your comment (required)</label>
      <textarea id="ccomment" name="comment" required></textarea>
    </p>
    <p>
      <input class="submit" type="submit" value="Submit">
    </p>
  </fieldset>
</form>
<script>
	$("#commentForm").validate();
</script>
```
### Isn't that nice and easy?

A single line of jQuery to select the form and apply the validation plugin, plus a few annotations on each element to specify the validation rules.

Of course that isn't the only way to specify rules. You also don't have to rely on those default messages, but they come in handy when starting to setup validation for a form.

### A few things to look out for when playing around with the demo

* After trying to submit an invalid form, the first invalid element is focused, allowing the user to correct the field. If another invalid field – that wasn't the first one – was focused before submit, that field is focused instead, allowing the user to start at the bottom if he or she prefers.
* Before a field is marked as invalid, the validation is lazy: Before submitting the form for the first time, the user can tab through fields without getting annoying messages – they won't get bugged before having the chance to actually enter a correct value
* Once a field is marked invalid, it is eagerly validated: As soon as the user has entered the necessary value, the error message is removed
* If the user enters something in a non-marked field, and tabs/clicks away from it (blur the field), it is validated – obviously the user had the intention to enter something, but failed to enter the correct value

That behaviour can be irritating when clicking through demos of the validation plugin – it is designed for an unobtrusive user experience, annoying the user as little as possible with unnecessary error messages. So when you try out other demos, try to react like one of your users would, and see if the behaviour is better then. If not, please let me know about any ideas you may have for improvements!