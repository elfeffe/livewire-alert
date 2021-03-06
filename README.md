
# Livewire Alert

A very simple alerts utility for your existing livewire components. This package uses SweetAlert2 out-of-the-box. [https://sweetalert2.github.io/](https://sweetalert2.github.io/).

If you just want to show simple yet good-looking alert messages with nice animations this is for you!

![preview](https://raw.githubusercontent.com/jantinnerezo/livewire-alert/master/toast-preview.gif?token=AHC4OVKI6SNQ6DYWJ3AQQQK64WW6G)
![preview](https://raw.githubusercontent.com/jantinnerezo/livewire-alert/master/popup-preview.gif?token=AHC4OVKI6SNQ6DYWJ3AQQQK64WW6G)


## Installation

You can install the package via composer:

```bash

composer require jantinnerezo/livewire-alert

```

### Requirements

This package uses `livewire/livewire` (https://laravel-livewire.com/) under the hood.
Please make sure you include  it in your dependencies before using this package.

### Usage

First, add the `LivewireAlert` trait to your livewire component.
``` php

use  Livewire\Component;
use  Jantinnerezo\LivewireAlert\LivewireAlert;

class YourAwesomeComponent extends  Component
{
	use  LivewireAlert;
}

```
You should include `@livewireAlertScripts`  after `@livewireScripts`.

Let say you want to display a success alert message when a user successfully submitted a form:
``` php

public function submit()
{
	$this->alert('success', 'Submission successful!');
}

```

Example available events:

``` php
// Success event
$this->alert('success', 'Submission successful!');

// Information event
$this->alert('info', 'Hello, Awesome Developer!');

// Warning event
$this->alert('warning', 'You have been warned!');

// Error event
$this->alert('error', 'Whoops! you did it again!');

```
### Configuration
The default configurations:
``` php
[
	'position'  =>  'top-end',
	'timer'  =>  3000,
	'toast'  =>  true,
	'text' => null,
	'showCancelButton'  =>  true,
	'showConfirmButton'  =>  false
]
```
Here's an example of overriding the default configurations:

``` php
// Success event
$this->alert('success', 'You are successful!', [
	'position'  =>  'center',
	'timer'  =>  15000,
	'toast'  =>  false,
	'text'  =>  'I am a subtext',
	'showCancelButton'  =>  false,
	'showConfirmButton'  =>  false
]);
```
For more details about the configuration, see:
[https://sweetalert2.github.io/#configuration](https://sweetalert2.github.io/#configuration)
### Testing



``` bash

composer test

```



### Changelog



Please see [CHANGELOG](CHANGELOG.md) for more information what has changed recently.



## Contributing



Please see [CONTRIBUTING](CONTRIBUTING.md) for details.



### Security



If you discover any security related issues, please email erezojantinn@gmail.com instead of using the issue tracker.



## Credits



-  [Jantinn Erezo](https://github.com/jantinnerezo)

-  [All Contributors](../../contributors)



## License



The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
