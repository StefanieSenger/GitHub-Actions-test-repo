# GitHub-Actions-test-repo

Place where I play with GitHub Actions.

#### Notes
- link to github reference on [Events that trigger workflows](https://docs.github.com/en/actions/reference/events-that-trigger-workflows#about-events-that-trigger-workflows)

#### Tutorial
First, I had followed this FreeCodeCamp tutorial: [Learn to Use GitHub Actions: a Step-by-Step Guide](https://www.freecodecamp.org/news/learn-to-use-github-actions-step-by-step-guide/).
I've found a few mistakes in it, that I point put in case you're new to that, too:
- the folder where to define actions needs to be `.github/workflows`, not `.github/workflow`
- the linked [YAML tutorial](https://www.freecodecamp.org/news/what-is-yaml-the-yml-file-format/) shows an example of nested sequences, but it looks like the inner sequence had a name ("Javascript"); it seems though that sequences always go unnamed in YML
    - instead of this:
    ```
    - HTML
    - CSS
    - JavaScript
        - React
        - Angular
        - Vue
    ```
    - that seems to be correct (to my current knowledge):
    ```
    - HTML
    - CSS
    - JavaScript:
        - React
        - Angular
        - Vue
    ```