srpm:
	dnf -y install rpm-build rpmdevtools
	mkdir -p /builddir/build/SOURCES
	cp -p * /builddir/build/SOURCES/ 2>/dev/null || :
	spectool -g -C /builddir/build/SOURCES $(spec)
	rpmbuild -bs --define "_sourcedir /builddir/build/SOURCES" --define "_srcrpmdir $(outdir)" $(spec)
