# Docker-Calcardbackup

[![Build Status](https://travis-ci.org/Cyconet/docker-calcardbackup.svg?branch=development)](https://travis-ci.org/Cyconet/docker-calcardbackup)
[![Docker Build Status](https://img.shields.io/docker/build/waja/calcardbackup.svg)](https://hub.docker.com/r/waja/calcardbackup/)
[![GitHub tag](https://img.shields.io/github/tag/Cyconet/docker-calcardbackup.svg)](https://github.com/Cyconet/docker-calcardbackup/tags)
[![](https://img.shields.io/docker/pulls/waja/calcardbackup.svg)](https://hub.docker.com/r/waja/calcardbackup/)
[![](https://img.shields.io/docker/stars/waja/calcardbackup.svg)](https://hub.docker.com/r/waja/calcardbackup/)
[![](https://img.shields.io/docker/automated/waja/calcardbackup.svg)](https://hub.docker.com/r/waja/calcardbackup/)

## Usage:

  docker container run -d \
    --link mysql
    --volume /path/to/my/backup/folder:/backup
    waja/calcardbackup

## Variables

    CRON_TIME       the interval of cron job to run mysqldump. `0 0 * * *` by default, which is every day at 00:00
    INIT_BACKUP     if set, create a backup when the container starts
    BACKUP_DIR      location where the backup should be stored
    NC_DIR          location where Nextcloud config/config.php is searched for
    CALCARD_OPTS    options passed to calcardbackup
