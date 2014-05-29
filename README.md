# Translations for the meteor account's error messages

Right now only accounts-base and accounts-passwords are translated. Contributions for other packages are welcome. We try to translate only messages that might pop up at a users screen as developers are expected to understand English errors anyway.
Some translations have moved to accounts-entry, but translations can be added here for other accounts related modules and of course for more languages.

Translations are currently available for Czech, German, Italian, Polish and Spanish.

This package is inspired by just-i18n and included this as a dependency before version 0.0.3.

# API

##  Set a current language for translations: 
`T9n.language = "es"`

##  Set a default language to look up if nothing is found for the current language (defaults to "en"): 
`T9n.defaultLanguage = "en"`


## Get a translation in Javascript:

`T9n.get(code)`

Examples:
* `T9n.get('name');`
* `T9n.get('store.purchase');`
* `T9n.get('error.accounts.User not found');`

## Get a localized text in Handlebars

`{{t9n code}}`

Example: `{{t9n "store.purchase"}}`.

If a translation is not found the key is displayed. To spot not translated keys a prefix and a postfix can surround
the key, they default to ">" and "<" so a you would see ">nonExistantKey<". You can change the pre- and postfix: 

`T9n.missingPrefix = ">"`
`T9n.missingPostfix = "<"`


## Define translations

`T9n.map language, yourMap`

Example:

    T9n.map 'en',
      hello: 'world'
      store:
        purchase: 'buy now'
        basket: 'basket'

# Contributions
* mdede - Czech Translation
* robhunt3r - Improved Spanish Translation
* splendido - Italian Translation, Reactivity, Ideas
* pwldp - Polish Translation
* ryw - Fix for Blaze

# License

MIT
