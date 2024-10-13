# Avocado Impala
## How to generate SSH key?
1. `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"` <br>
If ask file straight away press enter, then key in the passphrase <br>
3. `eval "$(ssh-agent -s)"`
4. `ssh-add ~/.ssh/id_rsa`
5. `clip < ~/.ssh/id_rsa.pub`
6. Then navigate to `GitHub > Settings > SSH & GPG keys > New SSH Key`, paste the key, then add SSH key.

## After cloning the repo...
1. Open prompt
2. Run `cd [path to "avocada_impala directory"]`
3. Create a new environment in local machine <br>
Run `python -m venv venv`, and activate it by running `source venv/Scripts/activate`, set up the environment with the packages in `requirements.txt` by running: <br>
`pip install -r requirements.txt` <br>
4. If wanna install a new package in environemnt, you need to update the `requirements.txt` by running `pip freeze > requirements.txt` <br>
** Please inform everyone if you have installed a new package!
5. After you pull the updated `requirements.txt`, you need to update your local environment as well by running `pip install -r requirements.txt`

## How to push?
Before you wanted to push, please deactivate the venv by running `deactivate` <br>
1. `git add .`
2. `git commit -m "Write your commit msg here"`
3. `git push -u origin main`

## How to pull?
1. `git pull origin main`

