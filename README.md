# ECVC-SVN
The hub for Assembla's [ECVC](https://www.assembla.com/ecvc) enhancements to open-source Subversion software.

## Current Project: Shelving
Shelving means setting your uncommitted changes aside, so that you can work on something else. Shelving is fast and local, like 'git stash' and 'hg shelve' (and unlike Perforce's server-side shelving).

### Current status
This is the first public preview. It works. It only shelves text changes. See the design doc (linked below) for details.

Please get in touch and tell us: is it already useful enough, or what we must do to make it so?

### Shelving looks like...
![context menu](tsvn-1-cmenu-shelve.png)

![shelve dialog](tsvn-1-dlg-shelve.png)

![unshelve dialog](tsvn-1-dlg-unshelve.png)

![command line](shelve-demo-1.png)

### Try Shelving...
  * Windows: (unstable link)
    [TortoiseSVN-1.9.99.27998-dev-x64-svn-1.10.dev.msi](https://s3.amazonaws.com/assembla-binaries/TortoiseSVN/shelve/jobs/TSVN_shelve/18/TortoiseSVN-1.9.99.27998-dev-x64-svn-1.10.dev.msi)
  * MacOS: [command-line Subversion package](http://example.com/subversion-shelve.pkg)
  * Linux ...
  
### Tell us what you think about it...
* join the discussion: ...
* give your feedback: ...
* documentation: [Shelving and Checkpointing Dev.](https://docs.google.com/document/d/1PVgw0BdPF7v67oxIK7B_Yjmr3p28ojabP5N1PfZTsHk) (in Google Docs)
  * includes the rationale and the current limitations and possible extensions
  * you can add your comments in there too

## Assembla's Repositories on GitHub

### [assembla/subversion](https://github.com/assembla/subversion)
A central point for Assembla's contributions to [Apache Subversion](http://subversion.apache.org)
  * forked from a read-only [mirror repo](https://github.com/apache/subversion)
    (not automatically synchronized, so may be a little out of date)

### [assembla/tsvn](https://github.com/assembla/tsvn)
A central point for Assembla's contributions to [TortoiseSVN](http://tortoisesvn.net)
  * imported from the [TortoiseSVN master repo](https://sourceforge.net/p/tortoisesvn/code/)
    (not automatically synchronized, so may be a little out of date)
