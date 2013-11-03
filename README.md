# git-count

`git-count` is a git-subcommand that counts the number of lines of code that each author wrote.

## Installation

```sh
git clone https://github.com/neethouse/git-count.git
cd git-count
cp git-count <path/to/bin>
# "<path/to/bin>" is directory that included "$PATH".
```

### Use homebrew

```sh
brew tap neethouse/neet
brew install git-count
```

## How to use

### 1. Execute following command.

```sh
#only Objective-C files.
git count . "\.[hm]$"

# . is directory.
# "\.[hm]$" is egrep regex.
```
### 2. You'll get a nice siesta time.

( ˘ω˘ ) ｽﾔｧ…

### 3. You can get the rankings.

```
533 files found.

mironal       20564
mtmta         11794
ryohey        3072
YanaC         427
```

### 4. 晒しあげ (☝◞‸◟)☝


## Help

```
usage: git count <path> [<regex>]

CAUTION !!

Is very time consuming, if the repository is large.

OPTIONS

    <path>
        Attempt to counts the file hierarchy rooted in each file.

        e.g.
            Following the "src" directory.   -> git count "path/to/src"
            Following the "test" directory.  -> git count "path/to/test"
            Following the current directory. -> git count "."

    <regex>
        If you specify this regex pattern.
        You can count lines that files that match the regular expression.
        This regex pattern is the egrep regex pattern.

        e.g.
            Following the "src" directory.   -> git count "path/to/src"
            Only Java source code.  -> git count "." "\.java$"
            Only Scala source code. -> git count "." "\.scala$"
            Only Objective-C code.  -> git count "." "\.[hm]$"

        Or

        You can use default regex from git-config.

        git config --local git-count.regex "your regex pattern"
        git config --global git-count.regex "your regex pattern"

        Commandline argument takes precedence.

For more information -> "https://github.com/neethouse/git-count"
```

## Tips

### Use default regex pattern

You can use default regex from git-config.

`git config --local git-count.regex "your regex pattern"`

or

`git config --global git-count.regex "your regex pattern"`

Commandline argument takes precedence.
