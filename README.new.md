# Hurley Medical Center Site

## Physicians / Search

View the readme in `_search` to get python setup and installed.

Also, symlink the Dropbox photos dir to `_search/env/photos`.

__note:__ this was changed from the `_search/env` folder.

```bash
ln -s /path/to/the/dropbox/photos/folder _search/env/photos
```

## Building / Serving
### New Server 
To run Gulp you'll need to install needed dependencies.
Run which "cmd" to check for git, ruby, mysql, npm, nodejs.
Example: which ruby 
Follow the cmd list below to install all needed programs and dependencies. In this case CentOS uses yum, apt-get may need to be used depnding on your Linux flavor. 

'''bash
sudo yum install git

git clone https://github.com/connectedtech/hurleymc.connectedtech.com 

to path/to/hurley location

cd to path/to/hurley

# sudo yum install ruby
# sudo yum install ruby-devel
# gem install json_pure
# sudo yum install mysql
# sudo yum install mysql-devel
#
# sudo yum install npm or nodejs# If "no No package available." error presents run cmds from the next lines
## Note switch to root for following cmds
# rpm -Uvh https://mirror.webtatic.com/yum/el7/epel-release.rpm
# rpm -Uvh https://mirror.webtatic.com/yum/el7/webtatic-release.rpm
# Exit root and resume
# Run sudo yum install nodejs and npm again
##
# sudo npm install ## Note: npm install doesn't seem to install "gulp" correctly
# sudo npm install gulp -g # to fix this error
# gem install bundler
# bundle install # Note: Don't run as sudo or it will fail/break
# gulp or gulp serve
#
# #############################

### node / npm

Make sure you have node & npm installed, then install the required packages.

```bash
npm install
```

#### Gulp Tasks

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
