# Hurley Medical Center Site

## Building / Serving
## New Server 
To run Gulp you'll need to install needed dependencies.
Run which "cmd" to check for git, ruby, mysql, npm, nodejs.

(Ex: 'which ruby')

If you don't have those programs installed, follow the cmd list below to install all needed programs and dependencies. In this case CentOS uses yum, apt-get may need to be used depnding on your Linux flavor. 

```bash
sudo yum install git
```
###Creat Hurley folder

```
mkdir path/to/hurley
cd path/to/hurley
git clone https://github.com/connectedtech/hurleymc.connectedtech.com 
```

```bash
sudo yum install ruby
sudo yum install ruby-devel
gem install json_pure
```
###Mysql requires json_pure to install correctly. Once installed continue cmd list below. 
```
sudo yum install mysql
sudo yum install mysql-devel
sudo yum install nodejs
sudo yum install npm
```

###If "No package available" error presents for any 'yum install' switch to ROOT and run the cmds below.

```bash
rpm -Uvh https://mirror.webtatic.com/yum/el7/epel-release.rpm
rpm -Uvh https://mirror.webtatic.com/yum/el7/webtatic-release.rpm
```
###exit root and resume running the commands below.

```
sudo yum install nodejs
sudo yum install npm
sudo npm install 
```
###Note "npm install" may not install gulp correctly. Run "npm install -g" to correct. 
```
sudo npm install gulp -g
gem install bundler
bundle install    
```
###Note: don't run 'bundle install' as sudo/root or it will fail/break

```
gulp 
```
Congrats HurleyMC site should launch. Below are some cmds that should help with specific tasks.

## Physicians / Search

View the readme in `_search` to get python setup and installed.

Also, symlink the Dropbox photos dir to `_search/env/photos`.

__note:__ this was changed from the `_search/env` folder.

```bash
ln -s /path/to/the/dropbox/photos/folder _search/env/photos
```

### Gulp Tasks

These tasks will help automate the build process.

```bash
gulp
```
The default task which will serve the site with browsersync, along with rebuilding the site when necessary

```bash
gulp phys
```
This task will download all the physician data, crop and copy any physician photos, then build the site.

```bash
gulp deploy
```
This task will build the site, then deploy it to the gh-pages branch.

You can also run any of the other tasks that are in the `gulpfile.js` by themselves, but these are the main ones.
