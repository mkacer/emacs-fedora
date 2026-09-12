srpm:
	dnf -y install rpm-build spectool
	spectool -g -R $(spec)
	rpmbuild -bs --define "_sourcedir ." --define "_srcrpmdir $(outdir)" $(spec)
