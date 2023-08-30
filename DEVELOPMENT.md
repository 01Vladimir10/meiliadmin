## Prerequisites

You will need the following things properly installed on your computer.

* [Git](https://git-scm.com/)
* [Volta](https://volta.sh/) or [Node.js](https://nodejs.org/)
* [Ember CLI](https://cli.emberjs.com/release/)
* `Firefox` or `Google Chrome` (`Firefox` is better 😛)

## Installation

* `git clone <repository-url>` this repository
* `cd meiliadmin`
* `npm install`

## Running / Development

* `ember serve`
* Visit your app at [http://localhost:4200](http://localhost:4200).
* Visit your tests at [http://localhost:4200/tests](http://localhost:4200/tests).

### Code Generators

Make use of the many generators for code, try `ember help generate` for more details

### Running Tests

* `ember test`
* `ember test --server`

### Linting

* `npm run lint`
* `npm run lint:fix`

### Building

* `npm start` (development and watch)
* `npm run build` (production)
* `ROOTURL=/admin/ npm run build` (production build with rooturl, example: https://example.com/admin/)

## Further Reading / Useful Links

* [ember.js](https://emberjs.com/)
* [ember-cli](https://cli.emberjs.com/release/)
* Development Browser Extensions
  * [ember inspector for chrome](https://chrome.google.com/webstore/detail/ember-inspector/bmdblncegkenkacieihfhpjfppoconhi)
  * [ember inspector for firefox](https://addons.mozilla.org/en-US/firefox/addon/ember-inspector/)

## Install dummy Meilisearch instance
```bash
# Create folder
$ mkdir data && cd data

# Install Meilisearch
$ curl -L https://install.meilisearch.com | sh

# Download a dataset
$ curl https://raw.githubusercontent.com/meilisearch/documentation/main/assets/datasets/meteorites.json --output meteorites.json

# Start Meilisearch
$ ./meilisearch

# Create a new index `meteorites` and push the dataset
$ curl -X POST 'http://localhost:7700/indexes/meteorites/documents' -H 'Content-Type: application/json' --data-binary @meteorites.json
```

## Start Meilisearch instance
```bash
$ cd data && ./meilisearch --master-key="MASTER_KEY"
```
