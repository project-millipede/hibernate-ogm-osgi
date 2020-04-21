**The purpose of this repository is to execute CI/CD pipelines such as building,
testing, and deployment of a foreign repository.**

Changes to a repository will get tracked through Git`s submodule feature. A Git
submodule is defined by the URL of the remote repository and the branch name to
track.

> Why Git submodules and a custom CI/CD is relevant?

Is there any code pushed to this repository at all? Ideally, no.

Changes get applied in a remote repositories feature branch integrated through
Git`s submodule configuration.

Changes made on a feature branch are limited to address the problem of bundling
differentiation of various module systems, e.g., Java Module System and OSGi
differentiate.

> Why the repository embeds a custom CI/CD setup?

An essential aspect of every software project is CI/CD. Ideally, the original
project integrated through Git`s submodule provides a custom CI/CD strategy.

> Why repeating CI/CD?

Changes made in a feature branch have to pass the default test suite even
execute on a different CI/CD provider.

Using a separate and well understood CI/CD setup allows us to build custom
bundles and deploy it for further use.

1. Fork an existing Git project - (P1).
2. Create a secondary project - (P2).
3. Integrate the forked project (P1) in (P2) through Git`s submodule. Track the
   master branch.
4. Create a feature branch in the forked project (P1). Apply relevant changes.
5. Track the feature branch of P1 in Git`s submodule setup in P2.
6. Provide a custom CI/CD pipeline setup.

Repository: https://github.com/project-millipede/hibernate-ogm.git 
Branch: Master
