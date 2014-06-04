[![](docs/splash.png)](https://affirm.com) 

**Compatible with**

Magento CE 1.4.0.1+

Install
-------

**To install using [modgit](https://github.com/jreinke/modgit):**

```
cd MAGENTO_ROOT
modgit -i extension/:. add Magento_Affirm git@github.com:Affirm/Magento_Affirm.git
```
to update:
```
modgit update Magento_Affirm
```

**To install using [modman](https://github.com/colinmollenhour/modman):**

```
cd MAGENTO_ROOT
modman clone git@github.com:Affirm/Magento_Affirm.git
```
to update:
```
modman update Magento_Affirm
```

**To install using Affirm's deploy script:**

1. Download the [Makefile](https://raw.githubusercontent.com/Affirm/Magento_Affirm/master/util/Makefile) (requires git, wget)
2. Copy to MAGENTO_ROOT
3. To install, run `make install`
4. To update, run `make update`

Configure
---------

1. Log in to your Magento Admin portal.
2. Visit System > Configuration > Payment Methods (under Sales) > Affirm
3. Set the API URL. In a test environment, use ```https://sandbox.affirm.com```. On your live site, use ```https://www.affirm.com```.
4. Provide your 3 keys (merchant API key, secret key, financial product key)
5. Adjust the order total minimum and maximum options to control when Affirm is
   shown to your customers.
 
![](docs/config.png)


Contribute
----------

1. Fork the repo
2. Create your feature branch (```git checkout -b my-new-feature```).
3. Commit your changes (```git commit -am 'Added some feature'```)
4. Push to the branch (```git push origin my-new-feature```)
5. Create a Pull Request

**To run the tests:**

```
make dependencies
make test
```
