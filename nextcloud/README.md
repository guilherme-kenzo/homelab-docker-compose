# Nextcloud

This is a docker-compose install of nextcloud. Most of the steps are taken *verbatim* from the [nextcloud docker repo](https://github.com/nextcloud/docker#running-this-image-with-docker-compose) ― however, some changes were made to use compose version 3 instead of 2. 

# Updating

Aside from updating the container versions, some updates will require that the occ script is executed. The following snippet will be helpful:

```
docker exec -u 33 nextcloud_app_1 /var/www/html/occ upgrade
```

Note that the -u 33 executes the `/var/www/html/occ upgrade` command with the correct user (in my current install).