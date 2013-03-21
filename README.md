# Zeal

**zeal**  
*noun*  

 1. a feeling of strong eagerness (usually in favor of a person or cause)
 2. excessive fervor to do something or accomplish some end
 3. prompt willingness

(from WordNet 3.0)

Zeal is a simple documentation browser inspired by [Dash](http://kapeli.com/dash/).

![Screenshot](http://i.imgur.com/SiLvpz8.png)

[More screenshots (imgur)](http://imgur.com/a/eVi97)


## How to use

After installing/compiling it you need to download docsets. It can be done automatically by clicking 'Options', 'Docsets', 'Download...'.

Currently there are docsets available from Django, Ruby 1 and 2 [1], ExtJS 4.1, Python 2.7.3, Sencha Touch 2.1, Qt 5 [2].

[1] thanks to Dash's [docset exchange programme](https://github.com/jkozera/zeal/issues/1#issuecomment-13357189)  
[2] generated using scripts from `gendoctests` directory

You can also use Dash's docsets by putting `.docset` directories in `$HOME/.local/share/zeal/docsets/` (Linux) or `C:\Users\[your username]\AppData\Local\zeal\docsets\` (Windows).

## Binary packages

An [Ubuntu PPA](https://launchpad.net/~jerzy-kozera/+archive/zeal-ppa) is available with Ubuntu Quantal packages.

Also a 32-bit Windows binary with all dependencies is available to download from Dropbox - [zeal.zip](https://www.dropbox.com/s/aggp899jz2lzmfa/zeal.zip) (29M).

## How to compile

Currently Zeal requires Qt 5.0. To compile it, run `qmake` and `make` in the `zeal` directory.

## TODO

 * Support for global hotkeys under platforms other than Linux/X11 and Windows (OSX)
 * Search enhancements - some ideas:
   1. Allow selecting subset of docsets to search in.
   2. Grouping of similar results (like overloaded functions)
   3. Better docsets formatting (without headers, sidebars etc.)
 * More docsets
 * Code cleanup
   * `MainWindow::MainWindow` probably should be shorter than 200+ lines.
   * Refactoring to reuse common code between `ZealDocsetsRegistry` and `ZealListModel`

## Creating your own docsets

For creating new docsets, you have three choices of index format supported by Zeal.

 1. `ZEAL` format, as generated by scripts in `gendocsets` directory. It's essentially a single sqlite table with `type`, `name`, `path` and `parent` columns.
 2. `DASH` format, which is also similar single table, without the `parent` column.
 3. So-called `ZDASH`, which is a more complex Xcode docset format, implemented in Zeal to allow reusing Dash's docsets.

Author of Dash [has suggested](https://github.com/jkozera/zeal/issues/1#issuecomment-13357189) a "docset exchange programme", allowing Zeal to use one Dash docset in return for each new generated-for-Zeal docset, so it's recommended to use the `DASH` format.

## Contributions

Any feedback, feature requests, or pull requests are welcome. Before starting to implement anything larger, especially items from the TODO list above, it would be good to contact me at jerzy dot kozera at gmail, to avoid duplicating work.

Please keep in mind I'm not an experienced C++ programmer, so the code quality might be not great.

Also you can send bitcoins to 1Zea1QhPV5CGp8SNMpb2RHUvRrfNhKqGV to encourage development.


[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/jkozera/zeal/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

