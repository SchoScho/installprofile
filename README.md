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
    
6a) Two modules are missing, we have to add it still manually:

      cd /tmp
      git clone git@github.com:SchoScho/features.git 
      tar -xvf /tmp/features/indymedia_usermoderation_beta2-7.x-1.0-beta2.tar -C /var/www/drupal/sites/all/modules/
      tar -xvf /tmp/features/translationtool-7.x-1.0-beta1.tar -C /var/www/drupal/sites/all/modules/

7) Start apache and mysql

8) open http://localhost/drupal (or whereever your drupal installation is installed)

9) select de_indymedia_org installation profile

10) almost finished....

11) Stylesheet is still not at the install profile, we have to install it manually 

      cd site/all/themes
      git clone git@github.com:SchoScho/de.indymedia.org.drupal.css.git
