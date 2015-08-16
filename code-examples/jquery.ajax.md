# jQuery.ajax

Find below a simple way of using jQuery.ajax to verify an email address:

```javascript
// set endpoint and your access key
var access_key = 'YOUR_ACCESS_KEY';
var email_address = 'support@apilayer.net';

// verify email address via AJAX call
$.ajax({
    url: 'http://apilayer.net/api/check?access_key=' + access_key + '&email=' + email_address,   
    dataType: 'jsonp',
    success: function(json) {

    // Access and use your preferred validation result objects
    console.log(json.format_valid);
    console.log(json.smtp_check);
    console.log(json.score);
                
    }
});
```
  
