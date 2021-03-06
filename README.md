# R8PackageNameIssue
Reproduction project for R8 issue on Android issue tracker: https://issuetracker.google.com/u/0/issues/161227100

## Explanation
R8 version `2.0.88` (the default one bundled with Android Gradle plugin 4.0.0) strips out the package names from classes of Android library projects when `minify` is enabled:

![R8 2.0.88 strips out packages names](r8-2.0.88.png)

But forcing R8 version to 1.6.84 resolves the issue:

![R8 1.6.84 keeps packages names](r8-1.6.84.png)
