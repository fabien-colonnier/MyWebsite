# How to update the website

### Install Nikola

Check the nikola website to see if changes otherwise can follow the instructions below:
https://getnikola.com/getting-started.html

'''
mkdir -p ~/website/nikola
cd ~/website/nikola
virtualenv --python=python3 nikola
source ~/nikola/bin/activate
pip install --upgrade pip setuptools wheel
pip install --upgrade "Nikola[extras]"
deactivate
'''

### Download website

'''
git clone git@github.com:fabien-colonnier/MyWebsite.git
git checkout origin/src
'''

Need to have the ssh key uploaded
Change should be done in pages and file folder mostly

### Update website and preview the modification locally
'''
source ~/website/nikola/bin/activate
nikola build
nikola serve -b
'''

### create new page
'nikola new_page -f markdown'
(the title of the file will be written later)

### Upload the change
'''
nikola github_deploy -m "<commit msg>"
deactivate
'''
