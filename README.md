# Checkout

## What

A simple Ruby script to quickly switch between Git branches.

## How

1. Clone the project and symlink (or add) the checkout file to your bin or executable path.
1. Make the script executable `chmod +x checkout`

## Usage

Assuming you have the following branches:

```
master
develop
story-123/add_foo_to_bar
story-150/add_foo_to_biz
bug-10/fix_stuff
```

### Switching Branches

```
$ checkout 123
Switched to branch 'story-123/add_foo_to_bar'

$ checkout ma
Switched to branch 'master'

$ checkout -
Switched to branch 'story-123/add_foo_to_bar'

$ checkout add_foo

Found multiple branches:

0 - story-123/add_foo_to_bar
1 - story-150/add_foo_to_biz

Choose a number or anything else to cancel: 2

Switched to branch 'story-123/add_foo_to_biz'

```

### View History

```
$ checkout -h

[05/05/2017 10:39]    story-123/add_foo_to_bar
[05/05/2017 10:25]    master
[05/05/2017 10:23]    -
[05/05/2017 10:19]    story-150/add_foo_to_biz
```

### Clear History

```
$ checkout -hc
```

### Print Help

```
$ checkout --help

checkout {branch name}

-h     # Show history
-hc    # Clear file
--help # Print this message
```

