# Makefile for program source directory in GNU NLS utilities package.
# Copyright (C) 1995, 1996, 1997 by Ulrich Drepper <drepper@gnu.ai.mit.edu>
# Copyright (C) 2004-2008 Rodney Dawes <dobey.pwns@gmail.com>
#
# This file may be copied and used freely without restrictions.  It may
# be used in projects which are not available under a GNU Public License,
# but which still want to provide support for the GNU gettext functionality.
#
# - Modified by Owen Taylor <otaylor@redhat.com> to use GETTEXT_PACKAGE
#   instead of PACKAGE and to look for po2tbl in ./ not in intl/
#
# - Modified by jacob berkman <jacob@ximian.com> to install
#   Makefile.in.in and po2tbl.sed.in for use with glib-gettextize
#
# - Modified by Rodney Dawes <dobey.pwns@gmail.com> for use with intltool
#
# We have the following line for use by intltoolize:
# INTLTOOL_MAKEFILE

GETTEXT_PACKAGE = linphone
PACKAGE = linphone
VERSION = 3.5.0

SHELL = /bin/sh

srcdir = /Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/po
top_srcdir = /Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone
top_builddir = ..
VPATH = /Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/po

prefix = /Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//../liblinphone-sdk/armv7-apple-darwin
exec_prefix = ${prefix}
datadir = ${datarootdir}
datarootdir = ${prefix}/share
libdir = ${exec_prefix}/lib
DATADIRNAME = share
itlocaledir = $(prefix)/$(DATADIRNAME)/locale
subdir = po
install_sh = ${SHELL} /Users/chris/Code/Gargoyle/linphone-iphone/submodules/linphone/install-sh
# Automake >= 1.8 provides /opt/local/bin/gmkdir -p.
# Until it can be supposed, use the safe fallback:
mkdir_p = $(install_sh) -d

INSTALL = /opt/local/bin/ginstall -c
INSTALL_DATA = ${INSTALL} -m 644

GMSGFMT = /opt/local/bin/msgfmt
MSGFMT = /opt/local/bin/msgfmt
XGETTEXT = /opt/local/bin/xgettext
INTLTOOL_UPDATE = /opt/local/bin/intltool-update
INTLTOOL_EXTRACT = /opt/local/bin/intltool-extract
MSGMERGE = INTLTOOL_EXTRACT=$(INTLTOOL_EXTRACT) srcdir=$(srcdir) $(INTLTOOL_UPDATE) --gettext-package $(GETTEXT_PACKAGE) --dist
GENPOT   = INTLTOOL_EXTRACT=$(INTLTOOL_EXTRACT) srcdir=$(srcdir) $(INTLTOOL_UPDATE) --gettext-package $(GETTEXT_PACKAGE) --pot

ALL_LINGUAS = fr it de ja es pl cs nl sv pt_BR hu ru zh_CN nb_NO zh_TW

PO_LINGUAS=$(shell if test -r $(srcdir)/LINGUAS; then grep -v "^\#" $(srcdir)/LINGUAS; else echo "$(ALL_LINGUAS)"; fi)

USER_LINGUAS=$(shell if test -n "$(LINGUAS)"; then LLINGUAS="$(LINGUAS)"; ALINGUAS="$(ALL_LINGUAS)"; for lang in $$LLINGUAS; do if test -n "`grep '^$$lang$$' $(srcdir)/LINGUAS 2>/dev/null`" -o -n "`echo $$ALINGUAS|tr ' ' '\n'|grep '^$$lang$$'`"; then printf "$$lang "; fi; done; fi)

USE_LINGUAS=$(shell if test -n "$(USER_LINGUAS)" -o -n "$(LINGUAS)"; then LLINGUAS="$(USER_LINGUAS)"; else if test -n "$(PO_LINGUAS)"; then LLINGUAS="$(PO_LINGUAS)"; else LLINGUAS="$(ALL_LINGUAS)"; fi; fi; for lang in $$LLINGUAS; do printf "$$lang "; done)

POFILES=$(shell LINGUAS="$(PO_LINGUAS)"; for lang in $$LINGUAS; do printf "$$lang.po "; done)

DISTFILES = Makefile.in.in POTFILES.in $(POFILES)
EXTRA_DISTFILES = ChangeLog POTFILES.skip Makevars LINGUAS

POTFILES = \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/tunnel_config.ui \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/calllogs.c \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/conference.c \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/logging.c \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/support.c \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/chat.c \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/main.c \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/friendlist.c \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/propertybox.c \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/update.c \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/buddylookup.c \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/setupwizard.c \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/incall_view.c \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/loginframe.c \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/main.ui \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/about.ui \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/contact.ui \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/log.ui \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/password.ui \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/call_logs.ui \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/main.ui \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/sip_account.ui \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/chatroom.ui \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/parameters.ui \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/buddylookup.ui \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/gtk/waiting.ui \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/coreapi/linphonecore.c \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/coreapi/misc.c \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/coreapi/presence.c \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/coreapi/friend.c \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/coreapi/proxy.c \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/coreapi/callbacks.c \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/coreapi/sal_eXosip2.c \
	/Users/chris/Code/Gargoyle/linphone-iphone/submodules/build/..//linphone/coreapi/linphonecall.c

CATALOGS=$(shell LINGUAS="$(USE_LINGUAS)"; for lang in $$LINGUAS; do printf "$$lang.gmo "; done)

.SUFFIXES:
.SUFFIXES: .po .pox .gmo .mo .msg .cat

.po.pox:
	$(MAKE) $(GETTEXT_PACKAGE).pot
	$(MSGMERGE) $< $(GETTEXT_PACKAGE).pot -o $*.pox

.po.mo:
	$(MSGFMT) -o $@ $<

.po.gmo:
	file=`echo $* | sed 's,.*/,,'`.gmo \
	  && rm -f $$file && $(GMSGFMT) -o $$file $<

.po.cat:
	sed -f ../intl/po2msg.sed < $< > $*.msg \
	  && rm -f $@ && gencat $@ $*.msg


all: all-no

all-yes: $(CATALOGS)
all-no:

$(GETTEXT_PACKAGE).pot: $(POTFILES)
	$(GENPOT)

install: install-data
install-data: install-data-no
install-data-no: all
install-data-yes: all
	linguas="$(USE_LINGUAS)"; \
	for lang in $$linguas; do \
	  dir=$(DESTDIR)$(itlocaledir)/$$lang/LC_MESSAGES; \
	  $(mkdir_p) $$dir; \
	  if test -r $$lang.gmo; then \
	    $(INSTALL_DATA) $$lang.gmo $$dir/$(GETTEXT_PACKAGE).mo; \
	    echo "installing $$lang.gmo as $$dir/$(GETTEXT_PACKAGE).mo"; \
	  else \
	    $(INSTALL_DATA) $(srcdir)/$$lang.gmo $$dir/$(GETTEXT_PACKAGE).mo; \
	    echo "installing $(srcdir)/$$lang.gmo as" \
		 "$$dir/$(GETTEXT_PACKAGE).mo"; \
	  fi; \
	  if test -r $$lang.gmo.m; then \
	    $(INSTALL_DATA) $$lang.gmo.m $$dir/$(GETTEXT_PACKAGE).mo.m; \
	    echo "installing $$lang.gmo.m as $$dir/$(GETTEXT_PACKAGE).mo.m"; \
	  else \
	    if test -r $(srcdir)/$$lang.gmo.m ; then \
	      $(INSTALL_DATA) $(srcdir)/$$lang.gmo.m \
		$$dir/$(GETTEXT_PACKAGE).mo.m; \
	      echo "installing $(srcdir)/$$lang.gmo.m as" \
		   "$$dir/$(GETTEXT_PACKAGE).mo.m"; \
	    else \
	      true; \
	    fi; \
	  fi; \
	done

# Empty stubs to satisfy archaic automake needs
dvi info tags TAGS ID:

# Define this as empty until I found a useful application.
install-exec installcheck:

uninstall:
	linguas="$(USE_LINGUAS)"; \
	for lang in $$linguas; do \
	  rm -f $(DESTDIR)$(itlocaledir)/$$lang/LC_MESSAGES/$(GETTEXT_PACKAGE).mo; \
	  rm -f $(DESTDIR)$(itlocaledir)/$$lang/LC_MESSAGES/$(GETTEXT_PACKAGE).mo.m; \
	done

check: all $(GETTEXT_PACKAGE).pot
	rm -f missing notexist
	srcdir=$(srcdir) $(INTLTOOL_UPDATE) -m
	if [ -r missing -o -r notexist ]; then \
	  exit 1; \
	fi

mostlyclean:
	rm -f *.pox $(GETTEXT_PACKAGE).pot *.old.po cat-id-tbl.tmp
	rm -f .intltool-merge-cache

clean: mostlyclean

distclean: clean
	rm -f Makefile Makefile.in POTFILES stamp-it
	rm -f *.mo *.msg *.cat *.cat.m *.gmo

maintainer-clean: distclean
	@echo "This command is intended for maintainers to use;"
	@echo "it deletes files that may require special tools to rebuild."
	rm -f Makefile.in.in

distdir = ../$(PACKAGE)-$(VERSION)/$(subdir)
dist distdir: $(DISTFILES)
	dists="$(DISTFILES)"; \
	extra_dists="$(EXTRA_DISTFILES)"; \
	for file in $$extra_dists; do \
	  test -f $(srcdir)/$$file && dists="$$dists $(srcdir)/$$file"; \
	done; \
	for file in $$dists; do \
	  test -f $$file || file="$(srcdir)/$$file"; \
	  ln $$file $(distdir) 2> /dev/null \
	    || cp -p $$file $(distdir); \
	done

update-po: Makefile
	$(MAKE) $(GETTEXT_PACKAGE).pot
	tmpdir=`pwd`; \
	linguas="$(USE_LINGUAS)"; \
	for lang in $$linguas; do \
	  echo "$$lang:"; \
	  result="`$(MSGMERGE) -o $$tmpdir/$$lang.new.po $$lang`"; \
	  if $$result; then \
	    if cmp $(srcdir)/$$lang.po $$tmpdir/$$lang.new.po >/dev/null 2>&1; then \
	      rm -f $$tmpdir/$$lang.new.po; \
            else \
	      if mv -f $$tmpdir/$$lang.new.po $$lang.po; then \
	        :; \
	      else \
	        echo "msgmerge for $$lang.po failed: cannot move $$tmpdir/$$lang.new.po to $$lang.po" 1>&2; \
	        rm -f $$tmpdir/$$lang.new.po; \
	        exit 1; \
	      fi; \
	    fi; \
	  else \
	    echo "msgmerge for $$lang.gmo failed!"; \
	    rm -f $$tmpdir/$$lang.new.po; \
	  fi; \
	done

Makefile POTFILES: stamp-it
	@if test ! -f $@; then \
	  rm -f stamp-it; \
	  $(MAKE) stamp-it; \
	fi

stamp-it: Makefile.in.in $(top_builddir)/config.status POTFILES.in
	cd $(top_builddir) \
	  && CONFIG_FILES=$(subdir)/Makefile.in CONFIG_HEADERS= CONFIG_LINKS= \
	       $(SHELL) ./config.status

# Tell versions [3.59,3.63) of GNU make not to export all variables.
# Otherwise a system limit (for SysV at least) may be exceeded.
.NOEXPORT:
