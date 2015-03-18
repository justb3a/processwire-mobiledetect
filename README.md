# ProcessWire Mobile Detect

## Overview:

Mobile Detect uses a lightweight PHP class [(Mobile_Detect)](https://github.com/serbanghita/Mobile-Detect) for detecting mobile devices (including tablets). 

Designed for use with ProcessWire 2.4/2.5
[http://processwire.com](http://processwire.com)

## Installation:

1. Clone the module and place MobileDetect in your site/modules/ directory. 

```
git clone https://github.com/justonestep/processwire-mobiledetect.git your/path/site/modules/MobileDetect
```

2. Login to ProcessWire admin and click Modules. 
3. Click "Check for new modules".
4. Click "install" next to the new SimpleContactForm module. 

## Usage:

This Module extends `$config` and sets the following parameters:

```php
$config->mobileDetect = array(
  'deviceType' => 'deviceType (phone, tablet or desktop)',
  'browser' => 'mobile browser',
  'operatingsystem' => 'mobile operatingsystem',
  'device' => 'mobile device'
);
```

You can access them where ever you want.  
See the example below:

```html
  <body class="devicetype--<?php echo $config->mobileDetect->deviceType?>">
  <body class="devicetype--{{config.mobileDetect.deviceType}}"> // twig
```

Results in:

```html
<body class="devicetype--phone"> OR
<body class="devicetype--tablet"> OR
<body class="devicetype--desktop">
```
