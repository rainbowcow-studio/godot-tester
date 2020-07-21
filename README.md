# godot-tester

A Github Action to handle automated testing of Godot applications.

Assumes that you have installed and are using GUT as your testing framework.

## setup

Checkout your repository with actions/checkout then use this action.
The version of Godot you want to test against is required (e.g. "3.2.2")

Example workflow:

~~~ yaml

name: Godot testing

on: [ push ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2
    - uses: croconut/godot-tester@v1
      with:
        # required
        version: "3.2.2"
        is-mono: "true"
        # the folder with your projects.godot file in it
        path: "tester"

~~~~
