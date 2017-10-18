# ECVC-SVN
The hub for Assembla's [ECVC](https://www.assembla.com/ecvc) enhancements to open-source Subversion software.

## Current Project: Shelving
Shelving means setting your uncommitted changes aside, so that you can work on something else. Shelving is fast and local.

### Current status
This is the first public preview. It works. It only shelves text changes. See the design doc (linked below) for details.

Please get in touch and tell us what you think about it and where we should go next.

### Shelving looks like...
![context menu](tsvn-1-cmenu-shelve.png)

![shelve dialog](tsvn-2-dlg-shelve.png)

![unshelve dialog](tsvn-2-dlg-unshelve.png)

![command line](shelve-demo-1.png)

### Try Shelving...
  * Windows: (unstable link)
    [TortoiseSVN-1.9.99.27998-dev-x64-svn-1.10.dev.msi](https://s3.amazonaws.com/assembla-binaries/TortoiseSVN/shelve/jobs/TSVN_shelve/18/TortoiseSVN-1.9.99.27998-dev-x64-svn-1.10.dev.msi)
  * MacOS: [command-line Subversion package](http://example.com/subversion-shelve.pkg)
  * Linux:
    * Ubuntu ...
    * Debian ...
    * CentOS ...

### Understand Shelving
Shelving is a convenient way of creating and applying patches. It is similar in concept to 'git stash'.

The TortoiseSVN graphical interface is briefly described below.

The command-line interface is documented in `svn shelve --help` and `svn unshelve --help`. It is described, and compared with git/hg/bzr/p4, in [Shelving-Checkpointing UI](https://docs.google.com/document/d/1Z0HZfpWRnU0ke2G7H20V0-my_egV_BY4D_aGlfvKuTk/edit#heading=h.wkc757u986cn). It is very similar to [Mercurial Shelving (hg shelve)](https://www.selenic.com/mercurial/hg.1.html#shelve).

The central development doc: [Shelving and Checkpointing Dev.](https://docs.google.com/document/d/1PVgw0BdPF7v67oxIK7B_Yjmr3p28ojabP5N1PfZTsHk) includes the rationale and the current limitations and possible extensions.
  * you can add your comments in there too

#### Shelving and Unshelving in TortoiseSVN
The basic flow goes like this:
* You start with a version-controlled folder or file that contains some local (uncommitted) changes. Right-click; select `TortoiseSVN->Shelve`; enter a name; click *OK*. Subversion makes a patch (like with the `Create Patch` command) and saves the patch into `.svn/shelves/NAME.patch` and reverts those changes from your local files. That is "Shelving" your local changes.
* Then you might make some other changes, and shelve them with a different name.
* Then you want to restore the previously shelved changes back into your working files. Select `Unshelve` and select the name of the shelved change, click *OK*, and Subversion applies the patch (like using the `Apply Patch` command) and apparently deletes the patch.
  * (Actually it does not delete the patch file, it renames it to `NAME.patch.bak`.)

Much of the documentation for [Creating and Applying Patches in TortoiseSVN](https://tortoisesvn.net/docs/nightly/TortoiseSVN_en/tsvn-dug-patch.html) is relevant.
  
### Tell us what you think about it...
* join the discussion: ...
* give your feedback: ...

## Assembla's Repositories on GitHub

### [assembla/subversion](https://github.com/assembla/subversion)
A central point for Assembla's contributions to [Apache Subversion](http://subversion.apache.org)
  * forked from a read-only [mirror repo](https://github.com/apache/subversion)
    (not automatically synchronized, so may be a little out of date)

### [assembla/tsvn](https://github.com/assembla/tsvn)
A central point for Assembla's contributions to [TortoiseSVN](http://tortoisesvn.net)
  * imported from the [TortoiseSVN master repo](https://sourceforge.net/p/tortoisesvn/code/)
    (not automatically synchronized, so may be a little out of date)
