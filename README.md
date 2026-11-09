# Single-line Multiconditional

Combine two Skript conditions on one line using logical AND or OR.

## Requirements

- Skript 2.15+
- skript-reflect 2.6+

## Installation

```
package install https://github.com/devdinc/singleline-multiconditional
```

## Syntax

```skript
<condition> && <condition>
<condition> || <condition>
boolean value of condition <condition>
```

- `&&` is true only when both conditions are true.
- `||` is true when either condition is true.
- `boolean value of condition` evaluates a condition and returns its result as a boolean expression.

Each side is parsed as a normal Skript condition.

## Examples

```skript
if {_player} is set && {_player} is online:
    send "Welcome back!" to {_player}

if {_count} is 0 || {_count} is not set:
    set {_count} to 0

set {_valid} to boolean value of condition {_input} is a number
```

## Source and tests

- Implementation: `src/singleline-multiconditional.sk`
- Tests: `-tests/`
