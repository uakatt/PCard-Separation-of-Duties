PCard Separation of Duties
======================

This git repository represents the University of Arizona (the UA)'s _PCard Separation of Duties_ modification to **KFS 3.0**, in the form of patch files (generated by svn diff), liquibase scripts, and documentation.
This "patch package" is designed to be informative to technical developers in the position to
apply patch files to the java source code of KFS. In order to better serve such an endeavor,
this README contains several informative sections:

* <a href="#jiras">List of Jiras</a> - This list contains every Jira ticket at the University of Arizona
  that relates to this modification. It provides reverse documentation back to the developers at
  the UA in case of questions regarding how this patch package was created.
* <a href="#liquibase_changesets">List of Liquibase Changesets</a> - This list contains any
  liquibase changeset files that were associated with this modification.
* <a href="#patch_files">List of Patch Files</a> - This is a list of each patch file that needs
  to be applied to the KFS source code in order to realize the modification. This list does _not_
  include patch files for revisions that didn't touch the `trunk/` at the UA.
  Before a modification was merged with `trunk/`, it may have been tweaked, reworked, refactored,
  code reviewed, etc, in handfuls of revisions in a feature branch.
* <a href="#revisions">List of Revisions</a> - This list contains every revision associated with
  this modification. Many of which, as you will see, only touch files in a feature branch. The
  revisions that actually made it into the actual modification touch files in `trunk/`. The list
  of patch files is a better reference of which are these revisions.
* <a href="#files">Lists of Files</a> - These lists contain every file that was created,
  modified, or deleted for this enhancement.
* <a href="#post_mod_changes">List of Post-Modification Changes</a> - This list contains
  revision numbers that are _not_ included in the patches, or raw patches, but that touched one
  or more key files involved in this modification.

<h2><a name="jiras">Jiras</a></h2>

This is a list of Jira tickets at the University of Arizona that relate to this modification. The subversion revisions tagged against each such jira are also listed:

* **KITT-909**: (The main jira for this modification)<br />
  revisions: #9201

<h2><a name="liquibase_changesets">Liquibase Changesets</a></h2>

There are no liquibase changesets associated with this modification.

<h2><a name="patch_files">Patch Files</a></h2>

This is a list of all of the patches for revisions that affected files in `trunk/`. The filenames in each has been modified, for easy digestion. UA's subversion server manages many Kuali projects in one Subversion project, so a file path like:

```
financial-system/kfs/trunk/src/org/kuali/kfs...
```

has been modified to:

```
src/org/kuali/kfs...
```

* [`patches/09201_KITT-909_cleaned.diff`](PCard-Separation-of-Duties/blob/master/patches/09201_KITT-909_cleaned.diff) is the patch file for #9201.

<h2><a name="revisions">Revisions</a></h2>

This is an ordered list of revisions that relate to this modification. There may not be a patch
file for every revision listed below for the following reasons:

* A revision might only affect a branch, perhaps one where development primarily took place. Any
  changes that finally made it into `trunk/` will be seen in revisions that specifically touch
  files in `trunk/`. Therefore, we do not create patch files for revisions that only affect a
  branch.
* A revision might only include a liquibase changeset that is executed by some automated process.
  Since each institution maintains different revision controls on their database, liquibase
  changesets are not provided as patches. They are instead presented as intact files under the
  `liquibase-changesets/` directory.

[Here](PCard-Separation-of-Duties/blob/master/patch_log.txt) is a printout of `svn log -v` for each revision.

*   \#9201 was committed against KITT-909 on 2010-04-14 18:26:30 UTC by <strong>jwingate</strong>.

    > KITT-909 Prevent Cardholder Self Reconciliation

<h2><a name="files">Files</a></h2>

Files **modified** for this modification (4 files)

    /financial-system/kfs/branches/mod-jwingate/work/src/arizona-ApplicationResources.properties
    /financial-system/kfs/branches/mod-jwingate/work/src/com/rsmart/kuali/kfs/fp/document/ProcurementCardDocument.java
    /financial-system/kfs/branches/mod-jwingate/work/src/com/rsmart/kuali/kfs/fp/document/validation/impl/ProcurementCardHolderDetailRule.java
    /financial-system/kfs/branches/mod-jwingate/work/src/com/rsmart/kuali/kfs/fp/identity/ProcurementCardReconcilerDerivedRoleTypeServiceImpl.java

<h2><a name="post_mod_changes">Post Mod Changes</a></h2>

For each file that was changed or added for this modification, I've looked at its history in subversion (`svn log <file_name>`) to find whether later fixes were committed against this modification that I might have missed. There were some :) They may be fixes to the modification, or further enhancements, or changes completely unrelated. Please contact the UA for more information about a given revision number, or Jira ticket. Here they are:

*   **#13583** touches /financial-system/kfs/branches/mod-jwingate/work/src/com/rsmart/kuali/kfs/fp/document/ProcurementCardDocument.java.

    > Merge from Trunk 9/27


(1 revisions)

The following files were ignored here:

    arizona-ApplicationResources.properties

This means, for example, that `arizona-ApplicationResources.properties` was changed for this modification, but `arizona-ApplicationResources.properties`'s history was not used to build this list of revisions.

