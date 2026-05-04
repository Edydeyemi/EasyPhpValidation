# Easy PHP Validation
An easy-to-use, lightweight PHP Validation Class

The following parameters are required-
1. The name of the form field
2. The value to be validated

All validation methods can be chained together i.e. 
````shell
$v->setField('product_category')->required($product_cat_id)->isNumeric()->notGreaterThan(10);
$v->setField('promo_period')->required($promo_period)->isDate()->dateNotBefore('2026-06-01')->dateNotAfter('2026-12-31');
````
Errors are contained in the $error property.

## Installation

### With Composer

````shell
composer require Edydeyemi/easyphpvalidation
````

//1. Create a new instance of the Class
````shell
$v = new EasyPhpValidation(); //Create a new instance of the class
````

//2. Set a field as required
````shell
$v->setField('product_name', $_POST["product_name"])->required();
````

//3. Check for or output any errors in the validation object
````shell
print_r($v->errors);
````
