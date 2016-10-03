git-xflow
=========

An extension to [git-flow](http://github.com/nvie/gitflow), which automatize some usual tasks related to repository operations.



Getting started
---------------

As *git xflow* extends *git flow*, it is required to know what *git flow* is about:

* [Vincent Driessen's branching model](http://nvie.com/posts/a-successful-git-branching-model/)
* [Jeff Kreeftmeijer's blog post about git-flow](http://jeffkreeftmeijer.com/2010/why-arent-you-using-git-flow/)
* [Daniel Kummer's git-flow cheatsheet](http://danielkummer.github.io/git-flow-cheatsheet/)

Of course, a knowledge of *git* is also required:

* [Git official documentation](https://git-scm.com/documentation)
* [GitHub git cheat sheet](https://services.github.com/kit/downloads/github-git-cheat-sheet.pdf)

*git xflow* automatizes some reccurent tasks with *git flow*, such as:

* `git xflow feature/release/hotfix close` to finish and push a feature/release/hotfix
* `git xflow staging` to merge the content of unfinished features into a staging (demonstration) branch
* `git xflow hotfix publish/pull` to publish and pull a hotfix
* and many more !

To get help, just type in a terminal : `git xflow`



Install git-xflow
-----------------

*git xflow* runs on Windows, Linux, and Mac OS. In facts, it runs everywhere *git* is able to run.

1. [Install git-flow](https://github.com/nvie/gitflow/wiki/Installation)
1. Clone or [download](https://github.com/golflima/git-xflow/archive/master.zip) git-xflow, then unzip files ...
1. Put files into a PATH listed folded ([see details for Windows and Linux](https://en.wikipedia.org/wiki/PATH_(variable)))
1. For Linux only, make *gix-flow* file executable with:
   * `chmod +x git-xflow`
1. Test it, type in a terminal : `git xflow`

*NB : File `gitflow-common` is taken from [git-flow](https://raw.githubusercontent.com/nvie/gitflow/develop/gitflow-common) directly,
you don't have to copy it if you use latest version of git-flow and have put file `git-xflow` in the same folder as git-flow files.*

*git-xflow requires Bourne Again Shell (bash).*



Command-line reference
----------------------

See [Command-line Reference.md](docs/Command-line Reference.md) in docs folder.



Quick overview of major git-xflow features
------------------------------------------

1. Start working on a new feature *A* by typing:
   * `git xflow feature start A`
1. Do some work and commit your changes with: `git commit`
1. Start working on another new feature *B*:
   * `git xflow feature start B`
1. Do some work and commit your changes with: `git commit`
1. Send your changes to *staging* branch, only for feature *A*, by typing:
   * `git xflow staging reset A` *(this will reset staging branch)*
1. Then, send your changes from feature *B* to *staging* by typing:
   * `git xflow staging merge B`
1. Review changes of feature *A* with a HTML file by typing:
   * `git xflow feature review A -t html`
1. Review changes of feature *B* with *less* file by typing:
   * `git xflow feature review B -t less`
1. Finish your work on your features by typing:
   * `git xflow feature close A B`
1. Eventually, reset your *staging* branch to a clean state (*develop*), by typing:
   * `git xflow staging reset`
1. Do a release *1.0.0* for your new features by typing:
   * `git xflow release start 1.0.0`
1. Share your work on this release *1.0.0* with your peers by typing:
   * `git xflow release publish 1.0.0`
1. Start working on a shared release *1.0.0* by typing:
   * `git xflow release pull 1.0.0`
1. Finish and publish release *1.0.0* by typing:
   * `git xflow release close 1.0.0`
1. Build a patch to deploy changed files on your remote server which does not have Git by typing:
   * `git xflow tag patch` *(will make a patch from previous published tag to the new one)*

__________________________________________________

Licence terms
-------------

*git-xflow* is published under the terms of [GNU Lesser General Public License v3](http://www.gnu.org/licenses/lgpl-3.0.html), see the [LICENSE](LICENSE) file.

Although the GNU LGPLv3 does not require you to share any modifications you make to the source code,
you are very much encouraged and invited to contribute back your modifications to the community, preferably in a Github fork, of course.

For a list of all contributors, please see the [AUTHORS](AUTHORS) file.



Support
-------

You can support this project with
[![Flattr](https://button.flattr.com/flattr-badge-large.png)](https://flattr.com/submit/auto?fid=0ywe2d&url=https%3A%2F%2Fgithub.com%2Fgolflima%2Fgit-xflow)