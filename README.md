# [Plugin Handle](https://github.com/annihilatoratm/prestashop-doc/tree/main?tab=readme-ov-file#prestashop-16-module-for-payneteasy-payment-gateway)
# [Payment Flow](https://github.com/annihilatoratm/joomla-doc/blob/main/doc-eng.md#payment-flow-1)

## Prestashop 1.6 Module for PaynetEasy Payment Gateway

### System Requirements

* PHP 5.3 - 5.5
* [curl extension](http://php.net/manual/en/book.curl.php)
* [Prestashop](http://www.prestashop.com/en/download) 1.6.x (the module has been tested with version 1.6.0.9)

### Implemented Functionality

This module allows processing payment via [Merchant PaynetEasy API](http://wiki.payneteasy.com/index.php/PnE:Merchant_API). The following payment methods are currently implemented:
- [x] [Sale Transactions](http://wiki.payneteasy.com/index.php/PnE:Sale_Transactions)
- [ ] [Preauth/Capture Transactions](http://wiki.payneteasy.com/index.php/PnE:Preauth/Capture_Transactions)
- [ ] [Transfer Transactions](http://wiki.payneteasy.com/index.php/PnE:Transfer_Transactions)
- [ ] [Return Transactions](http://wiki.payneteasy.com/index.php/PnE:Return_Transactions)
- [ ] [Recurrent Transactions](http://wiki.payneteasy.com/index.php/PnE:Recurrent_Transactions)
- [ ] [Payment Form Integration](http://wiki.payneteasy.com/index.php/PnE:Payment_Form_integration)
- [ ] [Buy Now Button integration](http://wiki.payneteasy.com/index.php/PnE:Buy_Now_Button_integration)
- [ ] [eCheck integration](http://wiki.payneteasy.com/index.php/PnE:eCheck_integration)
- [ ] [Western Union Integration](http://wiki.payneteasy.com/index.php/PnE:Western_Union_Integration)
- [ ] [Bitcoin Integration](http://wiki.payneteasy.com/index.php/PnE:Bitcoin_integration)
- [ ] [Loan Integration](http://wiki.payneteasy.com/index.php/PnE:Loan_integration)
- [ ] [Qiwi Integration](http://wiki.payneteasy.com/index.php/PnE:Qiwi_integration)
- [ ] [Merchant Callbacks](http://wiki.payneteasy.com/index.php/PnE:Merchant_Callbacks)

### Steps

* Install prestashop 1.6.1.24
* Transfer controllers and modules folders to root directory of installed Prestashop
* Advanced Parameters > Performance turn off cache and template completion, enable Disable all overrides setting.
* Install and setup paynet module(Modules and Services > Modules and Services).
* Clear product catalog(Catalog > Products) and add new via Add new product button. Do not forget to setup quantity and price.

### <a name="get_package"></a> Download package containing module

#### Bulding package manually
1. [Install composer](http://getcomposer.org/doc/00-intro.md), if it is not installed
2. Clone module source code: `composer create-project payneteasy/php-plugin-prestashop --stability=dev --prefer-dist`
3. Go to module source code directory: `cd php-plugin-prestashop`
4. Pack the module into archiver: `composer archive --format=zip`

### Install, Configure and Remove Module Instruction

#### Install Module


1. [Download package containing module](00-introduction.md#get_package)
2. Unpack the package into Prestashop root directory
3. Open Administration Panel of Prestashop
4. Go to list of modules (see arrow #1)
5. Install Module
    1. Enter "payneteasy" in the search box (see arrow #1)
    2. Install Module by pressing the "Install" button  (see arrow #2)
6. Confirm your intention to install the module, which is not related to verified modules (see arrow #1)


* [Configure Module](02-configuration.md)

#### Configure Module

1. Open Prestashop Administration Panel
2. Go to list of modules (see arrow #1)
3. Open the module settings page
    1. Enter "payneteasy" in the search box (see arrow #1)
    2. Open module setting page by pressing "Configure" button (see arrow #2)
4. Fill in the required settings of module and save them (arrow #1)

#### Remove Module

# Remove Module

1. Open Prestashop Administration Panel
2. Go to list of modules (see arrow #1)
3. Remove Module
    1. Enter "payneteasy" in the search box (arrow #1)
    2. Open the list of actions for the module (arrow #2)
    3. Choose "Delete" (arrow #3)
    4. 
## Payment Flow
