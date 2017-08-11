# dev-oracle

Quora-like question/answer forum for developers, with an emphasis on helping new developers in a non-nasty way.

## Planning

1. Configuration/dependencies
  * NPM/Ember
  * Bootstrap/SASS

2. Specs
  * Spec 1: Description, input, output.
  * Spec 2: Description, input, output.

3. Routes/Integration (a = action; b = button)
  * (route) index --> (loop) question-tile --> (link to) (route) question (a:destroyQ/destroyA/saveA)
      |-----> new-question (b:save/show)        |
                                                |-----> (component) update-question (b:save/update)
                                                |------> (component) question-detail (b:deleteQ) --> (loop) answer-tile (a:update/b:deleteA)
                                                |------> (component) new-answer (b:save/show)         |------> update-answer (b: save/update)
  * Components:
    * new-question: contains new question form, show/hide functionality, save question functionality
    * question-tile: contains question loop with question and author
    * question-detail: contains full question details (question, author, any other attributes)
    * update-question: contains update question form, show/hide functionality, save/update functionality, placeholders for current question data; only updates fields with inputted data
    * new-answer: contains new answer form, show/hide functionality, save answer functionality
    * answer-tile: contains answer loop with answer and author
    * update-answer: contains update question form, show/hide functionality, save/update functionality, placeholders for current answer data; only updates fields with inputted data

4. UX/UI
  * Include and modify Bootstrap/SASS etc.
  * Develop custom styles

5. Polish
  * Refactor minor portion of...
  * Delete unused...
  * Make README awesome

6. Wish List (if time)
  * Delete functionality for both questions and answers
  * User model
  * Admin panel

## Prerequisites

You will need the following things properly installed on your computer.

* [Git](https://git-scm.com/)
* [Node.js](https://nodejs.org/) (with NPM)
* [Ember CLI](https://ember-cli.com/)
* [PhantomJS](http://phantomjs.org/)

## Installation

* `git clone <repository-url>` this repository
* `cd dev-oracle`
* `npm install`

## Running / Development

* `ember serve`
* Visit your app at [http://localhost:4200](http://localhost:4200).

### Code Generators

Make use of the many generators for code, try `ember help generate` for more details

### Running Tests

* `ember test`
* `ember test --server`

### Building

* `ember build` (development)
* `ember build --environment production` (production)

### Deploying

Specify what it takes to deploy your app.

## Further Reading / Useful Links

* [ember.js](http://emberjs.com/)
* [ember-cli](https://ember-cli.com/)
* Development Browser Extensions
  * [ember inspector for chrome](https://chrome.google.com/webstore/detail/ember-inspector/bmdblncegkenkacieihfhpjfppoconhi)
  * [ember inspector for firefox](https://addons.mozilla.org/en-US/firefox/addon/ember-inspector/)
