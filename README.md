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


#### Configure Module

1. Open Prestashop Administration Panel
2. Go to list of modules by clicking on *Modules* -> *Module Manager* (1)
3. Open the module settings page
    1. Enter "payneteasy" in the search box to find the plugin (2)
    2. Open module setting page by pressing "Configure" button (3)
       
  <img src="/images/prestashop-1-1.png" width=60% height=60%>
  
4. Fill in the required settings of module and save them (arrow #1)
  <img src="/images/prestashop-1-2.png" width=60% height=60%>

#### Remove Module

1. Open Prestashop Administration Panel
2. Go to list of modules
3. Remove Module
    1. Enter "payneteasy" in the search box
    2. Open the list of actions for the module
    3. Choose "Delete"
       
  <img src="/images/prestashop-1-3.png" width=60% height=60%>

  ## Payment Flow

  1. On the main page choose a product. Once it chosen, press on *Add to cart* button to continue the flow.
  <img src="/images/prestashop-1.png" width=60% height=60%>
  <img src="/images/prestashop-2.png" width=60% height=60%>
  
  2. The pop-up message will indicate that the product was added to the card. You can *Proceed to checkout* to continue the payment process or *Continue Shopping* to return to the shop.

  <img src="/images/prestashop-popup.png" width=60% height=60%>

  3. Once you are ready for payment, click on *Cart* (1) icon at the top of the bar to examine the added items. Press on *Proceed to checkout* (2) to procees the payment.

  <img src="/images/prestashop-3.png" width=60% height=60%>

  4. All required parameters in Personal Information, Addresses, Shipping Method and Payment Method (Payneteasy must be used) sections have to be filled. Click on *Place order* button to finish the payment process.

  <img src="/images/prestashop-5.png" width=60% height=60%>
  <img src="/images/prestashop-6.png" width=60% height=60%>
