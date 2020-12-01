# react-unordered-list

initial exercise of [learn react js - full course for beginners - tutorial 2019](https://www.youtube.com/watch?v=DLX62G4lc44), in which we are asked to fill out the boiler plate for a basic react app. It is hosted [here](https://lagooned.github.io/react-unordered-list).

## steps
1. run npm init inside the dir
2. add react deps to package.json
3. adding react-scripts targets to steps in package.json
4. running npm start and amending to the project until it complies
5. adding basic html structure to public/index.html
6. add jsx to index.js to make unordered list
7. done

## ci addition
1. create github actions workflow [.github/workflows/node.js.yml](.github/workflows/node.js.yml)
2. setup normal node js steps:
  - git checkout
  - setup node
  - install npm deps via `npm ci`
  - run tests
    - use `react-scripts test --passWithNoTests` for projects with no test
      - defined in `packages.json` workflow scripts
  - run build (post test for efficiency)
  - deploy to gh pages
    - requires token setup in settings > developer options > Personal access token
    - create secret and store in repository and then inject into this stage via `jobs.build.steps.['deploy to gh pages'].env` hash
    - refer to this key in `jobs.build.steps.['deploy to gh pages'].run`
