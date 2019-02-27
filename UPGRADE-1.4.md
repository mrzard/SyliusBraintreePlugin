# UPGRADE FROM `v1.3.X` TO `v1.4.0`

## Application

* Run `composer require sylius/sylius:~1.4.0 --no-update`

* Run `composer require symfony/dotenv:^4.2 --no-update`

* Run
    ```
    git mv tests/Application/.env.dist tests/Application/.env
    git mv tests/Application/.env.prod.dist tests/Application/.env.prod
    git mv tests/Application/.env. tests/Application/.env.prod
    ```

* Update PHP and JS dependencies by running `composer update` and `(cd tests/Application && yarn upgrade)`

* Clear cache by running `(cd tests/Application && bin/console cache:clear)`

* Install assets by `(cd tests/Application && bin/console assets:install public)` and `(cd tests/Application && yarn build)`
