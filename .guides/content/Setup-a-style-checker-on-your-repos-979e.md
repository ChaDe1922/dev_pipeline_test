##

**Note:** Use your repo from TODAY that has .py files.

1. Open the assignment in a new browser tab or clone the repo into this project.

1. Create a `.github` folder

1. Inside the `.github` folder, create a `workflows` folder

1. Inside the `workflows` folder, create a `.yaml` file

1. Paste the following into the `.yaml` file
    ```yaml
    name: Check Style
    on: push

    jobs:
      check-style:
        runs-on: ubuntu-18.04
        steps:
          - uses: actions/checkout@v1

          - name: Setup python
            uses: actions/setup-python@v2
            with:
              python-version: 3.6

          - name: Install tools
            run: python -m pip install --upgrade pip pycodestyle

          - name: Check Style
            run: pycodestyle --first *.py
    ```

1. Push changes to the repo

## Checking the Results

1. Go to Github and navigate to the repo you just pushed to

1. Click on the Actions tab

Need more help? 
https://docs.github.com/en/actions/quickstart#viewing-your-workflow-results