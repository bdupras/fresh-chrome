# fresh-chrome

Launch new instances of Google Chrome on OS X with their own empty cache, cookies, and user configuration.

```shell
% ./fresh-chrome help
Usage: fresh-chrome <command> [<args>]

Launch a new instance of Google Chrome with its own empty cache, cookies, and
user configuration.

Commands:
   init       Launch a new Google Chrome instance with a permanent user-data
              directory in /Users/brian.dupras/.fresh-chrome.  Any additional
              arguments are passed to Chrome.

              Example:
              fresh-chrome init \
                            --use-fake-ui-for-media-stream \
                            --use-fake-device-for-media-stream \
                            --no-default-browser-check \
                            --no-first-run

   up|start   Launch a new Google Chrome instance with a temporary user-data
              directory copied from the user-data directory set up by
              'fresh-chrome init'.  Additional arguments passed in 'fresh-chrome init'
              are passed by default to 'fresh-chrome up'.

              Examples:
              fresh-chrome up                ## starts Chrome with the same arguments used in 'fresh-chrome init.'
              fresh-chrome up --disable-java ## adds the --disable-java argument to the argument list used in 'fresh-chrome init.'

   down|stop  Kills all Chrome instances started by 'fresh-chrome up|start'
              and removes all temporary user-data directories.

   destroy    Removes permanent user-data directory created by 'fresh-chrome init'.
```

Derived from [stuartsierra/fresh-chrome.sh](https://gist.github.com/stuartsierra/6220797)
