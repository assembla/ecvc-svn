# ECVC-SVN
The hub for Assembla's [ECVC](https://www.assembla.com/ecvc) enhancements to open-source Subversion software.

## Current Project: Shelving
Shelving means setting your uncommitted changes aside, so that you can work on something else. Shelving is a fast, local,  convenient way of creating and applying patches, similar in concept to 'git stash'.

From the central Wiki page [Shelving and Checkpointing](https://cwiki.apache.org/confluence/display/SVN/Shelving+and+Checkpointing) you can read about the rationale and the current limitations and possible extensions. You can add your comments in there too.

### Current status
Shelving v1 is available in TortoiseSVN 1.10 and command-line Subversion 1.10. Shelving v1, based on patch files, supports basic kinds of changes including text file content and properties.

Recent developments of Shelving and Checkpointing are available in [Cornerstone 4](https://cornerstone.assembla.com/) and preview builds of command-line Subversion. Support for 'binary' files, and other improvements, are currently in development.

### Try Shelving...
Go to https://www.assembla.com/subversion to download for Windows, MacOS or Linux.

-- or --

Build the current development version of Subversion or TortoiseSVN from source, following the normal build procedure of those projects.

### How to Use Shelving in TortoiseSVN 1.10
Start with a version-controlled folder or file that contains some local (uncommitted) changes. Right-click; select `TortoiseSVN->Shelve`.

Enter a name; click *OK*. Subversion makes a patch (like with the `Create Patch` command) and saves the patch into `.svn/shelves/NAME.patch` and reverts those changes from your local files. That is Shelving your local changes.

Then you can make other changes and shelve them with a different name.

You can restore the previously shelved changes back into your working files. Select `TortoiseSVN->Unshelve` and select the name of the shelved change, click *OK*, and Subversion applies the patch (like using the `Apply Patch` command) and removes the patch.

See also: [Creating and Applying Patches in TortoiseSVN](https://tortoisesvn.net/docs/nightly/TortoiseSVN_en/tsvn-dug-patch.html).
  
![context menu](tsvn-1-cmenu-shelve.png)

![shelve dialog](tsvn-2-dlg-shelve.png)

![unshelve dialog](tsvn-2-dlg-unshelve.png)

### How to Use 'svn shelve' on the Command Line

The command-line interface is documented in `svn shelve --help` and `svn unshelve --help`. For information about the development, and a comparison with git/hg/bzr/p4, see [Shelving Command-Line UI Design](https://cwiki.apache.org/confluence/display/SVN/Shelving+Command-Line+UI+Design).

![command line](shelve-demo-1.png)
