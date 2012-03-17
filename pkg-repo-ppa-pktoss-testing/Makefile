distro=$(shell lsb_release -cs)

all:

install:
	install -d $(DESTDIR)/etc/apt/sources.list.d/
	install -d $(DESTDIR)/etc/apt/preferences.d/
	install -d $(DESTDIR)/usr/share/pkg-repo-ppa-pktoss-testing/
	install -m 644 *.list $(DESTDIR)/etc/apt/sources.list.d/
	install -m 600 30* $(DESTDIR)/etc/apt/preferences.d/
	install -m 600 *.gpg $(DESTDIR)/usr/share/pkg-repo-ppa-pktoss-testing/
	install -m 600 *.keys $(DESTDIR)/usr/share/pkg-repo-ppa-pktoss-testing/
	for i in *.list ; do sed -i 's/<release>/$(distro)/g' $(DESTDIR)/etc/apt/sources.list.d/$$i ; done

