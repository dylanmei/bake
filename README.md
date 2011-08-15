# Bake

Simple make utility for bash


## Installation

    npm install bake

or

    git clone https://github.com/mgutz/bake
    cd bake
    npm link

## Usage

Display tasks

    bake

Run a task

    bake <task>


## Example

Example Bakefile

    function _private {         # underscored functions do not display
        echo in private
    }

    function clean {            # cleans the project
        echo cleaning ...
        _private
    }

    function build {            # builds the project
        # invokes clean only once
        invoke "clean"
        echo building ...
    }



Tasks are simply functions.

A comment on the same line of the function displays in the task list.

Use `invoke` to invoke a task only once.

Functions prefixed with underscore `_` are not displayed in task list.
