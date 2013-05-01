installprofile
==============

installation profile to install de.indymedia.org

1) Download drupal 7.x and install it somewhere, like /var/www/drupal
Jump into profile directory of the drupal installation  
  cd /var/www/drupal/profiles
2) Clone git repository of the installation profile into this directory
  git clone git@github.com:SchoScho/installprofile de_indymedia_org
3) download and install drush , the drupal shell
  apt-get install drush
4) Init database: https://drupal.org/documentation/install/create-database
5) Adjust site/default/settings.php
6) call drush execution file
  cd /var/www/drupal
  drush make --force-complete profiles/de_indymedia_org/local.make.example
7) Start apache and mysql
8) open http://localhost/drupal (or whereever your drupal installation is installed)
9) select de_indymedia_org installation profile
10) finished.
