# Git PHP Lint

Require this with composer:

    php composer.phar require --dev m1ke/git-php-lint:dev-master

Unfortunately this uses the `post-install-cmd` script in composer, which doesn't trigger for required dependencies. Once you've updated your packages run:

    ./vendor/m1ke/git-php-lint/shell/setup

It will add a git `pre-commit` script to lint PHP files, via a symlink into the package.