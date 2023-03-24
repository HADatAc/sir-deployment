# sir-deployment
Docker environment for installing a DRUPAL container. Includes instructions for installing SIR GUI in Drupal

## How to run SIR-GUI and SIR-API?

# Deploy SIR-GUI Drupal module (in case you already have a Drupal website and SIR-API deployed)
1. SIRGUI's host machine requires the installation of `drupal` version 8 or 9 (https://www.drupal.org/)

2. Clone the SIRGUI repository (https://github.com/HADatAc/sir) into custom drupal modules folder.

3. To install the SIR-GUI Drupal module, run `drush en -y sir` or enable it using Drupal's admin panel.

4. Access http://YOURDRUPALSITE/admin/config/sir

5. Inform the SIR API Base URL IP Address and save the configuration

# Deploy SIR-GUI and SIR-API (in case you don't have neither drupal or SIR-API deployed)

1. SIRAPI's host machine requires the installation of `git` and `docker`

2. Using `git clone`, clone SIRAPI from github

3. Using `docker build .`, build SIRAPI images

4. Overwrite docker-compose.yml from SIR-API with the docker-compose.yml from SIR-GUI repository

5. Using `docker-compose up -d`, run the containers

6. Access http://YOURDRUPALSITE/admin/config/sir

7. Inform the SIR API Base URL IP Address and save the configuration
