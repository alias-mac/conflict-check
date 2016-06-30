# Vardef and View defs checker

This is the Sugar 7.8+ Vardef and View def checker.

## How to use the script

You can ask for help anytime by simply run:
```bash
$ ./conflict-check -h
```

You can run this with directories:

```bash
$ ./conflict-check -d="directory/to/check"
$ ./conflict-check --dir="directory/to/check"
```

Or files only:

```bash
$ ./conflict-check -f="file/to/check"
$ ./conflict-check --file="file/to/check"
```

Both can be have multiple values:

```bash
$ ./conflict-check -d="directory1/to/check" -d="directory2/to/check"
$ ./conflict-check -f="file1/to/check" -f="file2/to/check"
```

Directories can have regex patterns (that will be used by glob):

```bash
$ ./conflict-check -d="directory1/*/to/*/check"
```

For your convenience, you can keep the script out of the sugarcrm path and
combine the params above with the path of the [SugarCRM][SugarCRM] instance to
update:

```bash
$ ./conflict-check -p="path/to/sugarcrm" -d="directory/to/check"
$ ./conflict-check --path="path/to/sugarcrm" -d="directory/to/check"
```

To see more output information from the script, you can use the `-v` option
(for verbose).

```bash
$ ./conflict-check -p="path/to/sugarcrm" -d="directory/to/check" -v
```

You can even be bold and run the script directly from github:

```bash
$ curl -sS https://raw.github.com/alias-mac/conflict-check/master/conflict-check | php -- --path="path/to/sugarcrm" -f="modules/*/clients/*/views" -v
```

## Have fun!

## TODO

- [ ] Support some modules that are blacklisted.
- [ ] Support SugarObjects templates (like company, person, file, etc.).

[SugarCRM]: http://www.sugarcrm.com/
