# AUTOMATICALLY GENERATED -- DO NOT EDIT
BINDIR = $(EPREFIX)/bin
CC = cc
DATADIR = $(DATAROOTDIR)
DATAROOTDIR = $(PREFIX)/share
DOCDIR = $(DATAROOTDIR)/doc/$(PACKAGE)
EPREFIX = $(PREFIX)
INCLUDEDIR = $(PREFIX)/include
INFODIR = $(DATAROOTDIR)/info
INSTALL ?= /usr/bin/install
LD = cc
LIBDIR = $(EPREFIX)/lib
LIBEXECDIR = $(EPREFIX)/libexec
LOCALEDIR = $(DATAROOTDIR)/locale
LOCALSTATEDIR = $(PREFIX)/var
MANDIR = $(DATAROOTDIR)/man
OLDINCLUDEDIR = /usr/include
PKGCONFIGDIR = $(LIBDIR)/pkgconfig
PKGDATADIR = $(DATADIR)/$(PACKAGE)
PKGINCLUDEDIR = $(INCLUDEDIR)/$(PACKAGE)
PKGLIBDIR = $(LIBDIR)/$(PACKAGE)
PREFIX = /usr/local
SBINDIR = $(EPREFIX)/sbin
SHAREDSTATEDIR = $(PREFIX)/com
SYSCONFDIR = $(PREFIX)/etc


#
# Detect the canonical system type of the system we are building on
# (build) and the system the package runs on (host)
# 
BUILD_CPU=$(shell uname -m)
HOST_CPU=$(BUILD_CPU)
BUILD_VENDOR=unknown
HOST_VENDOR=$(BUILD_VENDOR)
BUILD_KERNEL=$(shell uname | tr '[A-Z]' '[a-z]')
HOST_KERNEL=$(BUILD_KERNEL)
BUILD_SYSTEM=gnu
HOST_SYSTEM=$(BUILD_SYSTEM)
BUILD_TYPE=$(BUILD_CPU)-$(BUILD_VENDOR)-$(BUILD_KERNEL)-$(BUILD_SYSTEM)
HOST_TYPE=$(HOST_CPU)-$(HOST_VENDOR)-$(HOST_KERNEL)-$(HOST_SYSTEM)

# Allow variables to be overridden via a ./configure script that outputs config.mk
# FIXME -- requires GNU Make
-include config.mk

default: all

all:  libkqueue.so libkqueue.a kqtest libkqueue.pc

check:  kqtest
	./kqtest

clean: 
	rm -f *.rpm
	rm -f libkqueue-2.0.tar.gz
	rm -f src/common/filter.o
	rm -f src/common/knote.o
	rm -f src/common/map.o
	rm -f src/common/kevent.o
	rm -f src/common/kqueue.o
	rm -f src/windows/timer.o
	rm -f src/windows/platform.o
	rm -f src/windows/read.o
	rm -f src/windows/user.o
	rm -f libkqueue.so
	rm -f libkqueue.a
	rm -f test/main.o
	rm -f test/kevent.o
	rm -f test/test.o
	rm -f test/read.o
	rm -f test/timer.o
	rm -f test/vnode.o
	rm -f test/user.o
	rm -f kqtest

config.h: 
	@echo "checking build system type... $(BUILD_TYPE)"
	@echo "checking host system type... $(HOST_TYPE)"
	@echo "/* AUTOMATICALLY GENERATED -- DO NOT EDIT */" > config.h.tmp
	@date > config.log
	@printf "checking whether EPOLLRDHUP is declared in sys/epoll.h... " | tee -a config.log
	@( printf '#define _GNU_SOURCE\n#include <sys/epoll.h>\nint main() { EPOLLRDHUP; }' | $(CC) $(CFLAGS) -E -x c - ) >/dev/null 2>>config.log && ( echo '#define HAVE_DECL_EPOLLRDHUP 1' >> config.h.tmp ; echo 'yes' ) || (echo '#define HAVE_DECL_EPOLLRDHUP 0' >> config.h.tmp ; echo 'no' )
	@printf "checking whether ppoll is declared in poll.h... " | tee -a config.log
	@( printf '#define _GNU_SOURCE\n#include <poll.h>\nint main() { ppoll; }' | $(CC) $(CFLAGS) -E -x c - ) >/dev/null 2>>config.log && ( echo '#define HAVE_DECL_PPOLL 1' >> config.h.tmp ; echo 'yes' ) || (echo '#define HAVE_DECL_PPOLL 0' >> config.h.tmp ; echo 'no' )
	@printf "checking for sys/epoll.h... "
	@( echo '#include <sys/epoll.h>' | $(CC) $(CFLAGS) -E -x c - ) >/dev/null 2>&1 && ( echo '#define HAVE_SYS_EPOLL_H 1' >> config.h.tmp ; echo 'yes' ) || (echo '/* #undef HAVE_SYS_EPOLL_H */' >> config.h.tmp ; echo 'no' )
	@printf "checking for sys/event.h... "
	@( echo '#include <sys/event.h>' | $(CC) $(CFLAGS) -E -x c - ) >/dev/null 2>&1 && ( echo '#define HAVE_SYS_EVENT_H 1' >> config.h.tmp ; echo 'yes' ) || (echo '/* #undef HAVE_SYS_EVENT_H */' >> config.h.tmp ; echo 'no' )
	@printf "checking for sys/eventfd.h... "
	@( echo '#include <sys/eventfd.h>' | $(CC) $(CFLAGS) -E -x c - ) >/dev/null 2>&1 && ( echo '#define HAVE_SYS_EVENTFD_H 1' >> config.h.tmp ; echo 'yes' ) || (echo '/* #undef HAVE_SYS_EVENTFD_H */' >> config.h.tmp ; echo 'no' )
	@printf "checking for sys/inotify.h... "
	@( echo '#include <sys/inotify.h>' | $(CC) $(CFLAGS) -E -x c - ) >/dev/null 2>&1 && ( echo '#define HAVE_SYS_INOTIFY_H 1' >> config.h.tmp ; echo 'yes' ) || (echo '/* #undef HAVE_SYS_INOTIFY_H */' >> config.h.tmp ; echo 'no' )
	@printf "checking for sys/signalfd.h... "
	@( echo '#include <sys/signalfd.h>' | $(CC) $(CFLAGS) -E -x c - ) >/dev/null 2>&1 && ( echo '#define HAVE_SYS_SIGNALFD_H 1' >> config.h.tmp ; echo 'yes' ) || (echo '/* #undef HAVE_SYS_SIGNALFD_H */' >> config.h.tmp ; echo 'no' )
	@printf "checking for sys/timerfd.h... "
	@( echo '#include <sys/timerfd.h>' | $(CC) $(CFLAGS) -E -x c - ) >/dev/null 2>&1 && ( echo '#define HAVE_SYS_TIMERFD_H 1' >> config.h.tmp ; echo 'yes' ) || (echo '/* #undef HAVE_SYS_TIMERFD_H */' >> config.h.tmp ; echo 'no' )
	@rm -f conftest.c conftest.o
	@echo "creating config.h"
	@mv config.h.tmp config.h

dist: libkqueue-2.0.tar.gz

distclean: clean 
	rm -f GNUmakefile
	rm -f libkqueue-2.0.tar.gz
	rm -f config.h
	rm -f config.yaml
	rm -f rpm.spec

distdir: 
	umask 22 ; mkdir -p '$(distdir)/src/common'
	umask 22 ; mkdir -p '$(distdir)/src/common/../posix'
	umask 22 ; mkdir -p '$(distdir)/src/common/../posix/../../include/sys'
	umask 22 ; mkdir -p '$(distdir)/src/common/../linux'
	umask 22 ; mkdir -p '$(distdir)/src/windows'
	umask 22 ; mkdir -p '$(distdir)/src/windows/../common'
	umask 22 ; mkdir -p '$(distdir)/src/windows/../common/../posix'
	umask 22 ; mkdir -p '$(distdir)/src/windows/../common/../posix/../../include/sys'
	umask 22 ; mkdir -p '$(distdir)/src/windows/../common/../linux'
	umask 22 ; mkdir -p '$(distdir)/include/sys'
	umask 22 ; mkdir -p '$(distdir)/test'
	umask 22 ; mkdir -p '$(distdir)/test/..'
	cp -RL src/common/filter.c src/common/private.h src/common/tree.h src/common/debug.h src/common/knote.c src/common/alloc.h src/common/map.c src/common/kevent.c src/common/kqueue.c $(distdir)/src/common
	cp -RL config.h GNUmakefile kqueue.2 libkqueue.pc.in configure configure.rb $(distdir)
	cp -RL src/common/../posix/platform.h $(distdir)/src/common/../posix
	cp -RL src/common/../posix/../../include/sys/event.h $(distdir)/src/common/../posix/../../include/sys
	cp -RL src/common/../linux/platform.h $(distdir)/src/common/../linux
	cp -RL src/windows/timer.c src/windows/platform.c src/windows/read.c src/windows/user.c $(distdir)/src/windows
	cp -RL src/windows/../common/private.h src/windows/../common/tree.h src/windows/../common/debug.h $(distdir)/src/windows/../common
	cp -RL src/windows/../common/../posix/platform.h $(distdir)/src/windows/../common/../posix
	cp -RL src/windows/../common/../posix/../../include/sys/event.h $(distdir)/src/windows/../common/../posix/../../include/sys
	cp -RL src/windows/../common/../linux/platform.h $(distdir)/src/windows/../common/../linux
	cp -RL include/sys/event.h $(distdir)/include/sys
	cp -RL test/main.c test/common.h test/kevent.c test/test.c test/read.c test/timer.c test/vnode.c test/user.c $(distdir)/test
	cp -RL test/../config.h $(distdir)/test/..

install: 
	/usr/bin/test -e $(DESTDIR)$(LIBDIR) || $(INSTALL) -d -m 755 $(DESTDIR)$(LIBDIR)
	$(INSTALL) -m 0644 libkqueue.so $(DESTDIR)$(LIBDIR)/libkqueue.so.0.0
	/usr/bin/test -e $(DESTDIR)$(INCLUDEDIR)/kqueue/sys || $(INSTALL) -d -m 755 $(DESTDIR)$(INCLUDEDIR)/kqueue/sys
	$(INSTALL) -m 644 include/sys/event.h $(DESTDIR)$(INCLUDEDIR)/kqueue/sys
	/usr/bin/test -e $(DESTDIR)$(MANDIR)/man2 || $(INSTALL) -d -m 755 $(DESTDIR)$(MANDIR)/man2
	$(INSTALL) -m 644 kqueue.2 $(DESTDIR)$(MANDIR)/man2
	/usr/bin/test -e $(DESTDIR)$(PKGCONFIGDIR) || $(INSTALL) -d -m 755 $(DESTDIR)$(PKGCONFIGDIR)
	$(INSTALL) -m 644 libkqueue.pc $(DESTDIR)$(PKGCONFIGDIR)
	rm -f $(DESTDIR)$(LIBDIR)/libkqueue.so
	ln -s libkqueue.so.0.0 $(DESTDIR)$(LIBDIR)/libkqueue.so
	rm -f $(DESTDIR)$(LIBDIR)/libkqueue.so.0
	ln -s libkqueue.so.0.0 $(DESTDIR)$(LIBDIR)/libkqueue.so.0
	ln -s kqueue.2 $(DESTDIR)$(MANDIR)/man2/kevent.2

kqtest: test/main.o test/kevent.o test/test.o test/read.o test/timer.o test/vnode.o test/user.o
	$(LD)  -o kqtest -L . -Wl,-rpath,. -L . $(LDFLAGS) test/main.o test/kevent.o test/test.o test/read.o test/timer.o test/vnode.o test/user.o -march=i686 -lws2_32 -lkqueue $(LDADD)

libkqueue-2.0.tar.gz: 
	rm -rf libkqueue-2.0
	mkdir libkqueue-2.0
	$(MAKE) distdir distdir=libkqueue-2.0
	rm -rf libkqueue-2.0.tar libkqueue-2.0.tar.gz
	tar cf libkqueue-2.0.tar libkqueue-2.0
	gzip libkqueue-2.0.tar
	rm -rf libkqueue-2.0

libkqueue.a: src/common/filter.o src/common/knote.o src/common/map.o src/common/kevent.o src/common/kqueue.o src/windows/timer.o src/windows/platform.o src/windows/read.o src/windows/user.o
ifneq ($(DISABLE_STATIC),1)
	$(AR) cru libkqueue.a src/common/filter.o src/common/knote.o src/common/map.o src/common/kevent.o src/common/kqueue.o src/windows/timer.o src/windows/platform.o src/windows/read.o src/windows/user.o
	$(RANLIB) libkqueue.a
endif

libkqueue.pc: config.h
	@echo 'creating libkqueue.pc'
	@printf "prefix=$(PREFIX)\nexec_prefix=$(EPREFIX)\nlibdir=$(LIBDIR)\nincludedir=$(INCLUDEDIR)\n" > libkqueue.pc
	@cat libkqueue.pc.in >> libkqueue.pc

libkqueue.so: src/common/filter.o src/common/knote.o src/common/map.o src/common/kevent.o src/common/kqueue.o src/windows/timer.o src/windows/platform.o src/windows/read.o src/windows/user.o
	$(LD)  -o libkqueue.so -shared -fPIC -L . -Wl,-soname,libkqueue.so.0 $(LDFLAGS) src/common/filter.o src/common/knote.o src/common/map.o src/common/kevent.o src/common/kqueue.o src/windows/timer.o src/windows/platform.o src/windows/read.o src/windows/user.o -march=i686 -lws2_32 $(LDADD)

package: clean libkqueue-2.0.tar.gz
	rm -rf rpm *.rpm
	mkdir -p rpm/BUILD rpm/RPMS rpm/SOURCES rpm/SPECS rpm/SRPMS
	mkdir -p rpm/RPMS/i386 rpm/RPMS/x86_64
	cp libkqueue-2.0.tar.gz rpm/SOURCES
	rpmbuild --define "_topdir `pwd`/rpm" -bs rpm.spec
	cp rpm.spec rpm/SPECS/rpm.spec
	rpmbuild --define "_topdir `pwd`/rpm" -bb ./rpm/SPECS/rpm.spec
	mv ./rpm/SRPMS/* ./rpm/RPMS/*/*.rpm .
	rm -rf rpm

src/common/filter.o: src/common/filter.c src/common/private.h config.h src/common/tree.h src/common/../posix/platform.h src/common/../posix/../../include/sys/event.h src/common/../linux/platform.h src/common/debug.h GNUmakefile
	$(CC) -DHAVE_CONFIG_H -I. -I./src/common -I./include -Wall -Wextra -Wno-missing-field-initializers -g -O2 -std=c99 -D_XOPEN_SOURCE=600 -o src/common/filter.o -fPIC -DPIC $(CFLAGS) -c src/common/filter.c

src/common/kevent.o: src/common/kevent.c src/common/private.h config.h src/common/tree.h src/common/../posix/platform.h src/common/../posix/../../include/sys/event.h src/common/../linux/platform.h src/common/debug.h GNUmakefile
	$(CC) -DHAVE_CONFIG_H -I. -I./src/common -I./include -Wall -Wextra -Wno-missing-field-initializers -g -O2 -std=c99 -D_XOPEN_SOURCE=600 -o src/common/kevent.o -fPIC -DPIC $(CFLAGS) -c src/common/kevent.c

src/common/knote.o: src/common/knote.c src/common/private.h config.h src/common/tree.h src/common/../posix/platform.h src/common/../posix/../../include/sys/event.h src/common/../linux/platform.h src/common/debug.h src/common/alloc.h GNUmakefile
	$(CC) -DHAVE_CONFIG_H -I. -I./src/common -I./include -Wall -Wextra -Wno-missing-field-initializers -g -O2 -std=c99 -D_XOPEN_SOURCE=600 -o src/common/knote.o -fPIC -DPIC $(CFLAGS) -c src/common/knote.c

src/common/kqueue.o: src/common/kqueue.c src/common/private.h config.h src/common/tree.h src/common/../posix/platform.h src/common/../posix/../../include/sys/event.h src/common/../linux/platform.h src/common/debug.h GNUmakefile
	$(CC) -DHAVE_CONFIG_H -I. -I./src/common -I./include -Wall -Wextra -Wno-missing-field-initializers -g -O2 -std=c99 -D_XOPEN_SOURCE=600 -o src/common/kqueue.o -fPIC -DPIC $(CFLAGS) -c src/common/kqueue.c

src/common/map.o: src/common/map.c src/common/private.h config.h src/common/tree.h src/common/../posix/platform.h src/common/../posix/../../include/sys/event.h src/common/../linux/platform.h src/common/debug.h GNUmakefile
	$(CC) -DHAVE_CONFIG_H -I. -I./src/common -I./include -Wall -Wextra -Wno-missing-field-initializers -g -O2 -std=c99 -D_XOPEN_SOURCE=600 -o src/common/map.o -fPIC -DPIC $(CFLAGS) -c src/common/map.c

src/windows/platform.o: src/windows/platform.c src/windows/../common/private.h config.h src/windows/../common/tree.h src/windows/../common/../posix/platform.h src/windows/../common/../posix/../../include/sys/event.h src/windows/../common/../linux/platform.h src/windows/../common/debug.h GNUmakefile
	$(CC) -DHAVE_CONFIG_H -I. -I./src/common -I./include -Wall -Wextra -Wno-missing-field-initializers -g -O2 -std=c99 -D_XOPEN_SOURCE=600 -o src/windows/platform.o -fPIC -DPIC $(CFLAGS) -c src/windows/platform.c

src/windows/read.o: src/windows/read.c src/windows/../common/private.h config.h src/windows/../common/tree.h src/windows/../common/../posix/platform.h src/windows/../common/../posix/../../include/sys/event.h src/windows/../common/../linux/platform.h src/windows/../common/debug.h GNUmakefile
	$(CC) -DHAVE_CONFIG_H -I. -I./src/common -I./include -Wall -Wextra -Wno-missing-field-initializers -g -O2 -std=c99 -D_XOPEN_SOURCE=600 -o src/windows/read.o -fPIC -DPIC $(CFLAGS) -c src/windows/read.c

src/windows/timer.o: src/windows/timer.c src/windows/../common/private.h config.h src/windows/../common/tree.h src/windows/../common/../posix/platform.h src/windows/../common/../posix/../../include/sys/event.h src/windows/../common/../linux/platform.h src/windows/../common/debug.h GNUmakefile
	$(CC) -DHAVE_CONFIG_H -I. -I./src/common -I./include -Wall -Wextra -Wno-missing-field-initializers -g -O2 -std=c99 -D_XOPEN_SOURCE=600 -o src/windows/timer.o -fPIC -DPIC $(CFLAGS) -c src/windows/timer.c

src/windows/user.o: src/windows/user.c src/windows/../common/private.h config.h src/windows/../common/tree.h src/windows/../common/../posix/platform.h src/windows/../common/../posix/../../include/sys/event.h src/windows/../common/../linux/platform.h src/windows/../common/debug.h GNUmakefile
	$(CC) -DHAVE_CONFIG_H -I. -I./src/common -I./include -Wall -Wextra -Wno-missing-field-initializers -g -O2 -std=c99 -D_XOPEN_SOURCE=600 -o src/windows/user.o -fPIC -DPIC $(CFLAGS) -c src/windows/user.c

test/kevent.o: test/kevent.c test/common.h include/sys/event.h test/../config.h GNUmakefile
	$(CC) -DHAVE_CONFIG_H -I. -g -O0 -Wall -Iinclude -Itest -g -O0 -o test/kevent.o $(CFLAGS) -c test/kevent.c

test/main.o: test/main.c test/common.h include/sys/event.h test/../config.h GNUmakefile
	$(CC) -DHAVE_CONFIG_H -I. -g -O0 -Wall -Iinclude -Itest -g -O0 -o test/main.o $(CFLAGS) -c test/main.c

test/read.o: test/read.c test/common.h include/sys/event.h test/../config.h GNUmakefile
	$(CC) -DHAVE_CONFIG_H -I. -g -O0 -Wall -Iinclude -Itest -g -O0 -o test/read.o $(CFLAGS) -c test/read.c

test/test.o: test/test.c test/common.h include/sys/event.h test/../config.h GNUmakefile
	$(CC) -DHAVE_CONFIG_H -I. -g -O0 -Wall -Iinclude -Itest -g -O0 -o test/test.o $(CFLAGS) -c test/test.c

test/timer.o: test/timer.c test/common.h include/sys/event.h test/../config.h GNUmakefile
	$(CC) -DHAVE_CONFIG_H -I. -g -O0 -Wall -Iinclude -Itest -g -O0 -o test/timer.o $(CFLAGS) -c test/timer.c

test/user.o: test/user.c test/common.h include/sys/event.h test/../config.h GNUmakefile
	$(CC) -DHAVE_CONFIG_H -I. -g -O0 -Wall -Iinclude -Itest -g -O0 -o test/user.o $(CFLAGS) -c test/user.c

test/vnode.o: test/vnode.c test/common.h include/sys/event.h test/../config.h GNUmakefile
	$(CC) -DHAVE_CONFIG_H -I. -g -O0 -Wall -Iinclude -Itest -g -O0 -o test/vnode.o $(CFLAGS) -c test/vnode.c

uninstall: 
	rm -f $(DESTDIR)$(LIBDIR)/libkqueue.so
	rm -f $(DESTDIR)$(INCLUDEDIR)/kqueue/sys/include/sys/event.h
	rm -f $(DESTDIR)$(MANDIR)/man2/kqueue.2
	rm -f $(DESTDIR)$(PKGCONFIGDIR)/libkqueue.pc