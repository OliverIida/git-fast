# git-fast

`git-fast` is a command-line tool that lets you stage, commit, and push changes to a Git repository with a single command:

```bash
a
```

There are alternatives like having a Shell script in your repo or using built-in Source Control, but I usually work in the terminal and entering `a` seemed much more convenient.

View at https://pypi.org/project/git-fast/

---

## Installation

Install directly from Pypi:

```bash
pip install git-fast
```

Local Installation in this repository:

```bash
pip install -e .
```

---

## Usage

When you run:

```bash
a
```

It automatically stages all changes in your current working directory and prompts to enter a commit message:

```bash
enter commit message: _
```

 - After writing a message and hitting ENTER, the changes are committed and pushed to the remote repo.<br>
 - Entering an empty commit message results in the program doing `git reset` and exiting.

---

## Modify, create your own package from this repo

```bash
git clone https://github.com/OliverIida/git-fast.git
# Modify the code, package names etc
pip install --upgrade build # download/update build tool
python -m build # build the package
pip install --upgrade twine # install/update Twine
twine upload dist/* # upload the package to Pypi
# enter your Pypi API token
# test - pip install {your-package-name}
```