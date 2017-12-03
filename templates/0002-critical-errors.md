# 2. Critical Errors

This ADR has been recorded retrospectively.

## Status

Accepted

## Context

Parse errors in a file does not stop the execution of project. If a spec file does not have parse error, the file is executed. See [here](0001-parse-errors.md) for more information.   
Some parse errors affect the execution of spec files. Such errors should halt execution.  


## Decision

Critical errors introduced. These errors stop the execution of specs.
Circular reference of concepts is a critical error. No specs are executed.

## Consequences


