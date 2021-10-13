# Model files for the OEREB cadaster

This is a mirror to keep track of the [model files](https://models.geo.admin.ch/V_D/OeREB/) in their
different versions. It contains the different branches:

- [master](https://github.com/openoereb/models) => always the most recent
- [0_9](https://github.com/openoereb/models/tree/0_9)
- [1_0](https://github.com/openoereb/models/tree/1_0)
- [2_0](https://github.com/openoereb/models/tree/2_0)

To update, in the moment no automatic process is provided. Because the federal repo does
provide files in a not stable automtically obtainable way. The use file names like
`OeREBKRM_V1_1_Codelisten_20170101.xml`. This makes it really difficult to provide automatic
approach.

Decision for this repository is, to provide stable file names as stable as possible.

**Therefor files are renamed!!!**

For instance the file `oerebkrm09gesetze.xml` is renamed to `OeREBKRM_Gesetze.xml` or 
`oerebkrm09.ili` is renamed to `OeREBKRM.ili`. All versioning is left for git and semver. This
should hopefully provide a reliable way to diff the versions and use this repo as base
for automatic processes.

The following steps are necessary:

1. `git clone https://github.com/openoereb/models.git`
2. `cd models`
3. choose the correct branch `git checkout 2_0`
4. download the files which changed => don't forget to rename to the matching path!
5. CHECK IF FILES ARE CORRECT (sometimes errors while download popin up)
6. `git add .`
7. `git commit . -m "downloaded newest version"`
8. `git push`
9. create a pull request (NOT on master)
10. after merge into the feature branch don't forget to draft a release!

To integrate a new version like 3.0 etc:

1. `git clone https://github.com/openoereb/models.git`
2. `cd models`
3. choose the correct branch `git checkout -b 3_0`
4. download the files which changed => don't forget to rename to the matching path!
5. CHECK IF FILES ARE CORRECT (sometimes errors while download popin up)
6. `git add .`
7. `git commit . -m "downloaded newest version"`
8. `git push`
9. create a pull request (ON master)
10. after merge into the master branch don't forget to draft a release!


Note:

Project on github is setup to protect all branches fitting the pattern `[0-9]_[0-9]`. So feature branches will be set
automatically and won't be deleted.
