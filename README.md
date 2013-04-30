installprofile
==============

installation profile to install de.indymedia.org

# Download drupal 7.x and install it somewhere, like /var/www/drupal
# Jump into profile directory of the drupal installation  
cd /var/www/drupal/profiles
# Clone git repository of the installation profile into this directory
git clone git@github.com:SchoScho/installprofile de_indymedia_org
# download and install drush , the drupal shell
apt-get install drush
# call drush execution file
cd /var/www/drupal/profiles
drush make local.make.example

# todo: Installation of the missing libraries
# Start apache and mysql, init database, adjust site/default/settings.php 
# Open browser and select de_indymedia_org install profile
