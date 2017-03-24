Introduction
------------

This directory contains all testsuites for all CSS specifications still using
the [CSS test harness][harness].

As the test harness relies on the largely undocumented(!) old CSS build system,
this directory has a number of test requirements specific to it:

 * support files for a given test must live in an adjacent `support` directory;

 * tests must have a [`<link rel=help>`][spec-link] pointing to what they are
   testing;

 * for each spec so linked, test filenames must be unique; and

 * support and reference files must have unique filenames within the entire
   `css` directory.


Odd Directories
---------------

There are a few special directories that do not map to specifications:

vendor-imports/ is a legacy directory where third parties historically imported
their tests that originate and are maintained in an external repo. Files in
this directory should never be modified in this repo, but should go through the
vendor's process to be imported here.

work-in-progress/ is a legacy directory that contains all the work that was
once submitted to the repo, but was not yet ready for review. As pull requests
are now used, no new files should be added here. The subdirectories here are
named by test author or contributing organization.


[harness]: https://test.csswg.org/harness/
[spec-link]: http://web-platform-tests.org/writing-tests/css-metadata.html#specification-links
