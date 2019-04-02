# Authorize.net-Laravel
Authorize.net payment gateway integration with Laravel 5.6
Authorize.net package installation with laravel 5.6.
Step 1. Unzip the packages.zip and put inside the App\ folder. path should be like this, App\Packages\Authorize\Authorize.php
and now 
"require-dev": {
"authorizenet/authorizenet": "~1.9.6"
}	
inside the composer.json and composer update.

Step 2. Inside config folder config/services.php, copy code and paste any where inside services.php 
'authorize' => [
'login' => 'YOUR_KEY',
'key' => 'YOUR_KEY',
],

Step 3. In which controller you are using just add "use App\Pakages\Authorize\Authorize;" 

Step 4. Now ready to use that's it
e.g for card charge use something like this, in your controller.
public function your_method_name () {
$card_data = [
'card_number' => '4242424242424242',
'card_expiry_year' => '2023',
'card_expiry_month' => '11',
'card_cvv' => '181',
'amount' => 100,
];
Step 5. Payment refund option will after 24 hours.
