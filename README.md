# github basics:

## Setup SSL

First Step is to check for existing 

```
$ ls -al ~/.ssh
# Lists the files in your .ssh directory, if they exist
```

1. Generate a new key:

```
$ ssh-keygen -t ed25519 -C "your_email@example.com"
```

Press enter to confirm deafult file to save key.

Passpahrase set or leave empty.

2. Add key to ssh-agent:

Check if ssh agent is running. When pid is returned agent is running.

```
$ eval "$(ssh-agent -s)"
```

Do add:

```
$ ssh-add ~/.ssh/id_ed25519
```

## Set remote for local repository

It is important to note that the local repository created below needs to be on branch main

```
echo "# basics" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:GianRothfuchs/basics.git
git push -u origin main
```


