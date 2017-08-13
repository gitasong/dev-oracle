# DevOracle (aka AskMeAnything)

Quora-like question/answer forum for developers, with an emphasis on helping new developers in a non-snarky way. Users will be able to view all questions, ask a new question, update questions, view a question's detail, and answer questions from other users.

#### By Nicole Freed

## Planning

1. Configuration/dependencies
  * NPM/Ember
  * Bootstrap/SASS

2. Specs
  * The program will allow users to ask a question (add a question) on the home page.
  * The program will display all questions on the home page, with the question and the name of the author.
  * The program will allow users to click on a question and go to another page containing the question details and additional information.
  * The program will allow users to edit existing questions.
  * The program will allow users to add answers to a question on that question's page.
  * The program will allow users to update existing answers (if time).
  * The program will allow users to delete questions and/or answers (if time).

3. Routes/Integration (a = action; b = button)
  * (route) index --> (loop) question-tile --> (link to) (route) question (a:destroyQ/destroyA/saveA)
      |-----> new-question (b:save/show)        |
                                                |-----> (component) update-question (b:save/update)
                                                |------> (component) question-detail (b:deleteQ) --> (loop) answer-tile (a:update/b:deleteA)
                                                |------> (component) new-answer (b:save/show)         |------> update-answer (b: save/update)
  * Components:
    * new-question: contains new question form, show/hide functionality, save question functionality
    * question-tile: contains question loop with question and author
    * question-detail: contains full question details (question, author, any other attributes), delete button (if time)
    * update-question: contains update question form, show/hide functionality, save/update functionality, placeholders for current question data; only updates fields with inputted data
    * new-answer: contains new answer form, show/hide functionality, save answer functionality
    * answer-tile: contains answer loop with answer and author, delete button (if time)
    * update-answer: contains update question form, show/hide functionality, save/update functionality, placeholders for current answer data; only updates fields with inputted data (if time)

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

* `git clone https://github.com/gitasong/dev-oracle`
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

## Known Bugs

App will currently save empty questions/answers if the reader clicks the `Add Question` or `Add Answer` button and clicks it again without entering anything.

## Support and Contact Details

You can contact me with questions or inquiries at gitasong@github.io.

## Technologies Used

* HTML 5
* CSS 3
* Bootstrap 3
* FontAwesome 4.7.0
* Google Fonts
* JavaScript 5
* Node.js 8.2.1
* npm (Node package manager) 5.3.0
* Ember-CLI 2.14.2
* Bower (front-end dependency manager) 1.8.0

## Further Reading / Useful Links

* [ember.js](http://emberjs.com/)
* [ember-cli](https://ember-cli.com/)
* Development Browser Extensions
  * [ember inspector for chrome](https://chrome.google.com/webstore/detail/ember-inspector/bmdblncegkenkacieihfhpjfppoconhi)
  * [ember inspector for firefox](https://addons.mozilla.org/en-US/firefox/addon/ember-inspector/)

### License

This project is licensed under the MIT license.

Copyright (c) 2017 Nicole Freed. All rights reserved.
