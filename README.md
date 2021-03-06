# IRCheck
IRCheck is a Node.js validation library developed for Iranian developers in order to help them to do some validations on their specific national data.

## Install & Usage
You can install the package via the following command:

`npm install ircheck`

### Usage
First you need to import the package:
```javascript
const IRCheck = require('ircheck');
```

Then you can use the available methods for different available validators:
```javascript
IRCheck.Phone.checkType('02191001848'); //returns 'LANDLINE'
IRCheck.Phone.normalizeMobile('+989121234567'); // returns '9121234567'
IRCheck.Postal.isPostalCodeValid('7634598734'); // returns 'TRUE'
IRCheck.National.isNationalCodeValid('4721016352'); // returns 'TRUE'
```

## Validators Availability
Currently, the following validators are available:
* [Iran Phone Numbers](#phone)
* [Iran Postal](#postal)
* [Iran National Codes](#national)

### Phone
Here’s a list of available methods:
* `checkType(number)`  Check whether if a number is a type of mobile or landline
* `isMobile(number)` Verify the input number is a type of mobile
* `isLandline(number)` Verify the input number is a type of landline
* `normalizeMobile(number)`  Normalize a mobile number as 9121234567
* `normalizeLandline(number)` Normalize a landline number as 2191001848
* `getProvinceData(province {String|Number})` Get province info from its area code or code name
* `getProvincesFromLandline(number)` Extract province data from a landline numbers

### Postal
Here’s a list of available methods:
* `isPostalCodeValid(postalCode {String})` Check if the entered postal code is valid

### National
Here’s a list of available methods:
* `isNationalCodeValid(nationalCode {String})` Check if the entered Iranian national code is valid


## History
### 0.3.6
* Company national code validation has been added.

### 0.3.0
* Postal code validation has been added into the library.
* National code validation has been added into the library.
* Updating README.md file.
* A few changes in the main file.

### 0.1.1
* Fixing typo errors in README.md file.

### 0.1.0
* Initial release

## Contribution
Any contribution is much appreciated. Make sure that you write and run tests before submitting PR.

## License
MIT licensed
Copyright (C) 2017 Jeff Mosawy, [http://jmosawy.com](http://jmosawy.com)
