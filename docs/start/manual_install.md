# Manual installation on an existing server

## Unpack the Hubzilla files into the root of your web server document area
If you copy the directory tree to your webserver, make sure that you include the
hidden files like .htaccess.

If you are able to do so, we recommend using git to clone the source
repository rather than to use a packaged tar or zip file.  This makes the
software much easier to update. The Linux command to clone the repository
into a directory "mywebsite" would be:

    git clone https://framagit.org/hubzilla/core.git mywebsite

and then you can pick up the latest changes at any time with:

    git pull

make sure folders `store/[data]/smarty3` and `store` exist and are
writable by the webserver:

    mkdir -p "store/[data]/smarty3"
    chmod -R 777 store

    This permission (777) is very dangerous and if you have sufficient
    privilege and knowledge you should make these directories writeable
    only by the webserver and, if different, the user that will run the
    cron job (see below). In many shared hosting environments this may be
    difficult without opening a trouble ticket with your provider. The
    above permissions will allow the software to work, but are not
    optimal.

The following directories also need to be writable by the webserver in order for certain
web-based administrative tools to function:

* `addon`
* `extend`
* `view/theme`
* `widget`

## Official addons
### Installation
Navigate to your website. Then you should clone the addon repository (separately). We'll give this repository a nickname of 'hzaddons'. You can pull in other hubzilla addon repositories by giving them different nicknames:

    cd mywebsite
    util/add_addon_repo https://framagit.org/hubzilla/addons.git hzaddons

### Updating
For keeping the addon tree updated, you should be on your top level website directory and issue an update command for that repository::

    cd mywebsite
    util/update_addon_repo hzaddons

Create searchable representations of the online documentation. You may do this
any time that the documentation is updated :

    cd mywebsite
    util/importdoc


