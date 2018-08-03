# Motivation

## We perform code reviews in order to improve code quality and benefit from positive effects on team and company culture

## * ***Committers are motivated*** by the notion of a set of reviewers who will look over the change request: the committer tends to clean up loose ends, consolidate TODOs, and generally improve the commit

## * ***Sharing knowledge*** helps development teams in several ways:

### - A code review explicitly communicates added/altered/removed functionality to team members who can subsequently build on the work done

### - The committer may use a technique or algorithm that reviewers can learn from. More generally, code reviewers help raise the quality bar across the organization

### - Reviewers may possess knowledge about programming techniques or the code base that can help improve or consolidate the change

### - Positive interaction and communication strengthens social bonds between team members

## * ***Consistency*** in a code base makes code easier to read and understand, helps prevent bugs and facilitates collaboration between regular and migratory developer species

## * ***Legibility*** of code fragments is hard to judge for the author whose brain child it is, and easy to judge for a reviewer who does not have the full context. Legible code is more reusable, bug-free and future-proof

## * ***Accidental errors*** as well as *** structural errors*** are often much easier to spot for critical reviewers with an outside perspective

## * ***Compliance*** and regulatory environments often demand reviews

# What to review

## Each development team should agree on its own approach

# When to review

## Code reviews should happen after automated checks have completed successfully, but before the code merges to the repository's mainline branch

# Preparing code for review

## * ***Scope and size***. Changes should have a narrow, well-defined, self-contained scope that they cover exhaustively

## * Only submit ***complete, self-reviewed*** and ***self-tested*** code reviews

## * *** Refactoring changes*** should not alter behavior

# Commit messages

## Capitalized, short (80 chars or less) summary

# Finding reviewers

## Consequently, code reviews need to be prompt (on the order of hours, not days), and team members and leads need to be aware of the time commitment and prioritize review time accordingly

# Purpose

## * ***Does this code accomplish the author's purpose?***

## * ***Ask questions***

# Implementation

## * ***Think about how you would have solved the problem***

## * ***Do you see potential for useful abstractions?***

## * ***Think like an adversary, but be nice about it***

## * ***Think about libraries or existing product code***

## * ***Does the change follow standard patterns?***

## * ***Does the change add compile-time or run-time dependencies(especially between sub-projects)?***

# Legibility and style

## * ***Think about your reading experience***

## * ***Does this code have TODOs?***

## * ***Does this code adhere to coding guidelines and code style?***

# Maintainability

## * ***Read the tests***

## * ***Does this code review introduce the risk of breaking test code, staging stacks, or integrations tests?***

## * ***Does this code need integration tests?***

## * ***Does this change break backward compatibility?***

## * ***Leave feedback on code-level documentation, comments, and commit messages***

## * ***Was the external documentation updated?***

# Security

## Verify that API endpoints perform appropriate authorization and authentication consistent with the rest of the code base

## Check for other common weaknesses, e.g. weak configuration, malicious user input, missing log events, etc

# Comments: concise, friendly, actionable

## Reviews should be concise and written in neutral language

## Critique the code, not the author

## When something is unclear, ask for clarification rather than assuming ignorance

## Avoid possessive pronouns, in particular in conjunction with evaluations: "my code worked before your change", "your method has a bug"

## Avoid absolute judgments:"this can never work", "this result is always wrong"

## Try to differentiate between suggestions, required changes and points that need discussion or clarification

## Consider providing links or pointers to in-depth explanations of a problem

# Responding to reviews

## Respond to every comment, even if it's only a simple "ACK" or "done". Explain why you made certain decisions, why some function exists, etc

## Fixes should be pushed to the same branch, but in a separate commit

# In-person code reviews
