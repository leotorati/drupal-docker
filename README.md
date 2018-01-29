# drupal-docker
Docker compose files for Drupal development.

## Containers
This implementation was based on [Docker4Drupal](https://docker4drupal.readthedocs.io/en/latest/)

- **db:** Database, Maria DB
- **php:** PHP and Drupal. Drush and Composer are installed.
- **apache:** Apache Server
- **pma:** PHP My Admin
- **traefik:** HTTP reverse proxy and load balancer - [traefik](https://hub.docker.com/_/traefik/)

## Domains

### Drupal 7
- **Site:** drupal7.localhost
- **PMA:** pma.drupal7.localhost

### Drupal 8
- **Site:** drupal8.localhost
- **PMA:** pma.drupal8.localhost

## Permissions issues
To solve permission issues, follow instructions by https://wodby.com/stacks/drupal/docs/local/permissions/

## Directory Structure
- **codebase:** Drupal and composer files.
- **database:** Database files. So we can remove database container without lost current database.
- **apache:** Contain apache container files.
- **php:** Contain PHP/Drupal container files.

## Notes
- Use composer to add new module (`compose require drupal/module`).
- Drupal docroot is under `web` directory.

## To Do
- [ ] Test *xdebug* and fix it if necessary
