# PyTest CodeRoad

PyTest Python test runner for Atom-CodeRoad.

### Setup

Install Python

    pip install -U pytest
    pip install tap.py


### Writing Tests

There are two parts your tests will need: a task number and a feedback message.

##### Task number

Class title specifying the task number: `class Test##`

      class Test01:
        # tests here

      class Test02:
        # tests here

##### Feedback message

Test method providing the feedback message and starting with `test_`

      class Test01:
        def test_b_is_not_true(self):
          assert b == True
          # fails with message "b is not true"

        def test_a_is_not_one(self):
          assert a == 1
          # fails with message "a is not one"


##### Loading Workspace Files

Workspace files (created by the user) can be loaded inside of comments

    # load('file.py')

These files will be loaded from the users working directory.

##### Loading Data Files

Data files can be by setting a second parameter to `true`.

    # load('path/to/data.py', true)

These files will load from the specified tutorial directory in *package.json*.

*package.json*

    config {
      tutorialDir: 'tutorial'
    }

##### Complete Example

See the [examples](//github.com/coderoad/pytest-coderoad) directory.
