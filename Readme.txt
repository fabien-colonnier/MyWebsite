### How to update the website

# Install Nikola

https://getnikola.com/getting-started.html

$ mkdir ~/nikola
$ cd ~/nikola
$ virtualenv --python=python3 nikola
$ source ~/nikola/bin/activate
$ pip install --upgrade pip setuptools wheel
$ pip install --upgrade "Nikola[extras]"
$ deactivate


# Update website

$ git clone <url>
$ git checkout src

Change should be done in pages and file folder

# create new page
$ nikola new_page -f markdown

$ nikola build
$ nikola serve -b

$ nikola github_deploy
$ deactivate
