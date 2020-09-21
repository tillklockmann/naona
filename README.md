# Naona (Kiswahili for 'I see')
A really simple template engine.
## install with composer
```  
composer require tillklockmann\naona:1.0.1
``` 

## usage

Create a views folder in the root dir to store the templates. 
Template files are supposed to have the following naming convention:

**template-name.view.php**

Instantiate the View class
```php
$view = new Naona\View;
```
Optionally you can set the path to the template folder:
```php
$view = new Naona\View('path\to\folder');
```
Display the template with ``` render() ``` .
```php
$view->template('index')->render();
```
Set template variables  ``` set(string key, mixed value) ```
```php
// Controller.php
$myTitle = 'Great Website';
$this->view->template('index')
    ->set('title', $myTitle)
    ->render();
```
In the template file
```php
// index.view.php
<h1><?= $title ?></h1>
```


