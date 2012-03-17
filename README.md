Packages encapsulating debian repositories
==========================================

This project contains packages that encapsulate debian repositories.
Each repository install consists of a file under sources.list.d
(containing the needed "deb " and "deb-src " lines), the repository
gpg keyring and possibly a file to put under preferences.d to denote
the desired pinning etc for the repository.

This infrastructure is useful mostly for repositories like medibuntu
that aren't accessible under the standard repository management commands
(like add-apt-repository / ppa-purge) or for repositories that have
specific pinning requirements (like my pktoss/testing ppa).
