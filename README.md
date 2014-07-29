# Git PHP Lint

Require this with composer:

    php composer.phar require --dev m1ke/git-php-lint:1.0.0

Unfortunately this uses the `post-install-cmd` script in composer, which doesn't trigger for required dependencies. Once you've updated your packages run:

    ./vendor/m1ke/git-php-lint/shell/setup

It will add a git `pre-commit` script to lint PHP files, via a symlink into the package.

#### Security Note

Symlinking to a shell script in a package which auto-upates could obviously be a risk. For this reason only install this package with a set version constraint; that way you'll get a fixed release which you can eyeball for security before you run it.