# validateMe
Simple jQuery validation plugin.

This plugin provides validation for your form. Currently it validates text field (checks it for emptyness), email field (it must have an '@' sign, a dot after, two or more symbols after dot, etc.) and phone field.

## Usage

This plugin uses HTML5 form features, so at first, you have to set right type for your input: `text` only for text fields, `tel` for phone number and `email` for e-mails, huh. Then it is neccessary to set `required` attribute for inputs, that you want to validate. Well, actually after that about 80-90% of browsers will validate your form even without enabled Javascript. But with this plugin validation will be a bit more strict. For submit button it is great to use button-tag, like this `<button type="submit" class="submit-btn">Submit!</button>`.

Then just select your form and fire this plugin:

    $('.form').validateMe();

Also, this plugin sets state of submit button — user can't submit form, while all of required fields are not filled correctly. Plugin detects `button` in form by itself, but if you use, for example, `<input type="submit" class="i-submit">` for submit button, there is need to set this parameter:

    $('.form').validateMe({
      submitBtn: '.i-submit'
    });
