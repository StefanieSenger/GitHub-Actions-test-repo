# GitHub-Actions-test-repo

Place where I play with GitHub Actions.

#### Notes
- link to github reference on [Events that trigger
  workflows](https://docs.github.com/en/actions/reference/events-that-trigger-workflows#about-events-that-trigger-workflows)
- link to [Workflow syntax for GitHub Actions](https://docs.github.com/en/actions/reference/workflow-syntax-for-github-actions)

#### Tutorial
First, I had followed this FreeCodeCamp tutorial: [Learn to Use GitHub Actions: a
Step-by-Step
Guide](https://www.freecodecamp.org/news/learn-to-use-github-actions-step-by-step-guide/).
I've found a few mistakes in it, that I point put in case you're new to that, too:
- the folder where to define actions needs to be `.github/workflows`, not
  `.github/workflow`
- the second demo (`demo2.yml` in this repo) seems to have several problems and cannot
  be run (`permissions` are listed as an event, which they are not, and having `uses`
  and `run` in the same step below is wrong as well, as you can have either one of
  these, but not both)
- the zip files action is not triggered when someone pushes to `main` but on release
- the linked [YAML
  tutorial](https://www.freecodecamp.org/news/what-is-yaml-the-yml-file-format/) shows
  an example of nested sequences, but it looks like the inner sequence had a name
  ("Javascript"); it seems though that sequences always go unnamed in YML
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