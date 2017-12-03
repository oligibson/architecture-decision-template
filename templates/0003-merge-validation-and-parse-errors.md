# 3. Merge Validation and Parse errors

This ADR has been recorded retrospectively.

## Status

Proposed

## Context

Parse errors would stop gauge execution, but validation errors would not stop the execution. This is changed execution is not halted for parse errors. See [here](0001-parse-errors.md) for more information. 
There is no need to have two types of errors show to the user anymore.

## Decision

Show both validation and parse errors as just errors to the user. 

## Consequences