# Design Decisions

- build using BDD/TDD (where practical)
- implement a Pixel class
- implement a InvalidColorError class to be used when the pixels colour is not valid
- build a CommandLineParser class to handle parsing the input from the REPL
- build a list of VALID_INPUTS and use to validate requests from the BitmapEditor
- build associated InvalidInputError and InvalidArgumentsError classes
- build a BitmapImage class which is created by the BitmapEditor class


# Problems

- had some issues knowing how to test the run method of the REPL loop in the BitmapEditor. When I tried to do this ended up replicating the REPL in the test on screen, so it was sitting waiting for input that was not what was intended or wanted - DISCUSS/TODO
- have one failing test, which I think needs to use mocks/stubs/doubles to get it to execute. Investigating with `binding.pry` gets the test to pass, indicating that the step for assigning the output from the call to `cli.parse_input('W') (an invalid command) is not being executed.
- on introspection I probably should have built this from the command line down, as opposed to from the Pixel back to the command line. Again this was driven by how I wanted to test/design as part of BDD/TDD.

# TODO
- build additional tests
- discuss with peers/mentor to understand how I could have built this cleaner
- refactor code 
- setup Reek/Rubocop/Rubycritic for better code analysis. Just had basic setup
- write a blog on the process outlining understanding of building a pure ruby project with BDD/TDD
