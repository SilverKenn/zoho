## Requirements

* Get yourself a [Zoho CRM account](https://www.zoho.com/crm/).
* [Register your application](https://www.zoho.com/crm/developer/docs/php-sdk/clientapp.html)
* PHP >= 5.6.4
* Laravel >= 6.*

## Installation

Add Zoho CRM to your composer file via the `composer require` command:

```bash
$ composer require asciisd/zoho
```

Or add it to `composer.json` manually:

```json
"require": {
    "asciisd/zoho": "0.0.1"
}
```

Zoho CRM's service providers will be automatically registered using Laravel's auto-discovery feature.

## Configuration

The defaults configuration settings are set in `config/zoho.php`. Copy this file to your own config directory to modify the values. You can publish the config using this command:

```bash
$ php artisan zoho:install
```

You'll need to add the following variables to your .env file. Use the credentials previously obtained registering your application.

```php
ZOHO_CLIENT_ID=
ZOHO_CLIENT_SECRET=
ZOHO_REDIRECT_URI=
ZOHO_CURRENT_USER_EMAIL=
```

Then, follow the next steps:
1. Go to [Zoho CRM Developer Console](https://accounts.zoho.com/developerconsole).
2. Under the Client previously registered, click the vertical three points then `Self Client`.
3. Enter the default scope , then click `View Code`
```
aaaserver.profile.READ,ZohoCRM.modules.ALL,ZohoCRM.settings.ALL
```    
> If you want to apply a different scope, see the [link](https://www.zoho.com/crm//developer/docs/api/oauth-overview.html#scopes)

4. Copy the generated code.

Finally, run the following command:

```bash
$ php artisan zoho:setup
```

Enter the previously generated code.

**Zoho CRM is ready to use.**

## License

[MIT License](https://opensource.org/licenses/MIT). Copyright (c) 2020, Asciisd

## Support

Contact:<br>
[asciisd.com](https://asciisd.com)<br>
aemad@asciisd.com<br>
+2-010-1144-1444