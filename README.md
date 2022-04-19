# GitHub backup script

The script requires a GitHub token and a destination directory. It then uses the token to populate the destination directory with clones of all the repositories the token can access.

Repeated runs only update the already existing backups and add new repositories, if any.

## Step 1: Installation

Install the required Python dependencies using `pip3`:

```
$ pip3 install -r requirements.txt
```

## Step 2: Configuring

### Create a token

For authorization you need to create a new personal GitHub token. You can do this from the GitHub settings, under the **Personal Access Tokens** tab.

### Create a configuration file

To run the script you need a JSON configuration file. For an example see the included file `config.json.example`.

```
{
    "token": "ADD-TOKEN-HERE",
    "directory": "~/backup/"
}
```

## Step 3: Run the Script

```
$ python3 backup.py config.json
```
