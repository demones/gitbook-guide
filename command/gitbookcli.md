查看帮助信息

`gitbook -h`

```
Usage: gitbook [options] [command]

  Commands:

    versions                          list installed versions
    versions:print                    print current version to use in the current directory
    versions:available                list available versions on NPM
    versions:install [version]        force install a specific version of gitbook
    versions:link [folder] [version]  link a version to a local folder
    versions:uninstall [version]      uninstall a specific version of gitbook
    versions:update [tag]             update to the latest version of gitbook
    help                              list commands for a specific version of gitbook
    *                                 run a command with a specific gitbook version

  Options:

    -h, --help               output usage information
    -V, --version            output the version number
    -v, --gitbook [version]  specify GitBook version to use
    -d, --debug              enable verbose error
```

输入以下命令查看更详细的帮助信息
`gitbook help`

```
build [book] [output] 	 build a book
    --format 	 Format to build to (Default is website; Values are website, json, ebook)
    --log 	 Minimum log level to display (Default is info; Values are debug, info, warn, error, disabled)

  pdf [book] [output] 	 build a book to pdf
    --log 	 Minimum log level to display (Default is info; Values are debug, info, warn, error, disabled)

  epub [book] [output] 	 build a book to epub
    --log 	 Minimum log level to display (Default is info; Values are debug, info, warn, error, disabled)

  mobi [book] [output] 	 build a book to mobi
    --log 	 Minimum log level to display (Default is info; Values are debug, info, warn, error, disabled)

  serve [book] 	 Build then serve a gitbook from a directory
    --port 	 Port for server to listen on (Default is 4000)
    --lrport 	 Port for livereload server to listen on (Default is 35729)
    --watch 	 Enable/disable file watcher (Default is true)
    --format 	 Format to build to (Default is website; Values are website, json, ebook)
    --log 	 Minimum log level to display (Default is info; Values are debug, info, warn, error, disabled)

  install [book] 	 install plugins dependencies

  init [directory] 	 create files and folders based on contents of SUMMARY.md
```
