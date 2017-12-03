# 1. Show all parse errors

This ADR has been recorded retrospectively.

## Status

Accepted

## Context

During execution of gauge project if parse errors are found, execution does not proceed. Once a parse error is found in a file, parsing of other files is also stopped.   
This becomes cumbersome for the user, as it takes multiple parses to fix all errors in the project.      

## Decision

All parse errors will be collected and shown to the user.  
If a parse error is found in a spec, only that spec is ignored and others are run.

## Consequences

Two go channels are created, one for collects all specs and another collects all parse results. This can be merged to use only one channel.
