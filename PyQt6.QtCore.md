# Advice from IRC
```
[16:33] <toofar> mparillo: no-one else has complained about it. I think that looks like pyqt hasn't been rebuilt against the new Qt binaries?
[16:34] <toofar> I guess I would 1) chack the pyqt comes from the same repo as Qt 2) consider switching back to the not-unstable one since we haven't tested anything on 6.5 3) or rebuild pyqt locally in a virtualenv
[17:31] *** Channel modes: no messages from outside, topic protection
[17:31] *** This channel was created on 5/19/21 9:51 AM.
[17:32] <mparillo> Thank you. I can always downgrade (I did that the last time kde-unstable broke qutebrowser, but the last time it was useful information getting ready for the next release. But based on your reply, in this case is more likely that my notification did not help prepare for the next release of Qt packages.
[17:38] <mparillo> IIRC, the compiler sent a patch upstream to Qt.
[17:39] <mparillo> Last time I reported breakage caused by an upgrade while including kde-unstable.
[17:40] <toofar> It's pretty easy these days to build pyqt yourself in a virtualenv if you want to try https://www.riverbankcomputing.com/static/Docs/PyQt6/installation.html#building-and-installing-from-source
```

# Symptom
```
$ qutebrowser --temp-basedir
Fatal error: PyQt6.QtCore is required to run qutebrowser but could not be imported! Maybe it's not installed?

The error encountered was:
/usr/lib/python3.10/site-packages/PyQt6/QtCore.abi3.so: undefined symbol: _ZN16QCoreApplication13compressEventEP6QEventP7QObjectP14QPostEventList, version Qt_6

Please search for the python3 version of PyQt6.QtCore in your distributions packages, or see https://github.com/qutebrowser/qutebrowser/blob/master/doc/install.asciidoc

If you installed a qutebrowser package for your distribution, please report this as a bug.
```
