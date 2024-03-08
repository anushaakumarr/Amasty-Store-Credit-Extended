# Magento 2 - Amasty Store Credit Module Extended

**Amasty-Store-Credit-Extended is an extension of Amasty Store Credit that has additional APIs.** 
This extension helps you to add/remove store credit to the customer through REST API without the need of Magento Admin UI. All you need is an admin token to use this API.

## 1. How to install

Run the following command in Magento 2 root folder:

```
composer require amasty-extended/store-credit
php bin/magento setup:upgrade
php bin/magento setup:static-content:deploy
```

**Note:**
Amasty-Store-Credit-Extended requires installing [Amasty Store Credit](https://amasty.com/docs/doku.php?id=magento_2:store-credit-and-refund) in your Magento installation.

## 2. How to use

After installing, the package. And running the commands mentioned above. You can use the below API to add/remove store credit for the customer.

- Set REST API endpoint as `http://<magento2-server>/rest/V1/storecredit/addorsubtract` in url box and method as `POST`.
- Use Admin Token.
- Example:
    ```
    {
        "customerId": 1,
        "amount": 10.0, // to remove 10 store credit => -10.0
        "action": 13,
        "message": "Message"
    }
    ```

## 4. Contribute to this module

Feel free to **Fork** and contribute to this module and create a pull request so we will merge your changes main branch.

## 5. Get Support

- Feel free to mail to anushaakumarr@gmail.com if you have any further questions.
