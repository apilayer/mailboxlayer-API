# PHP cURL

Find below a simple way of using PHP (cURL) to verify an email address:

```php

// set API Access Key
$access_key = 'YOUR_ACCESS_KEY';

// set email address
$email_address = 'support@apilayer.net';

// Initialize CURL:
$ch = curl_init('http://apilayer.net/api/check?access_key='.$access_key.'&email='.$email_address.'');  
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);

// Store the data:
$json = curl_exec($ch);
curl_close($ch);

// Decode JSON response:
$validationResult = json_decode($json, true);

// Access and use your preferred validation result objects
$validationResult['format_valid'];
$validationResult['smtp_check'];
$validationResult['score'];

```
