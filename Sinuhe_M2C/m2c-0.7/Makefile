# This file is generated automatically! Change `Makefile.tmpl'!
#
# This file is part of Modula-2 translator.
#
#
# Makefile is verbose because it was written for pure `make' from
#   second version of ultrix.
#
SHELL=/bin/sh

# The subdirectory used for copying sources and creation of 
# compressed distribution tar file.
distdir = m2c-0.7

# The directory for the sources being compiled.
# The value of this varaible is set up by `configure'.
srcdir = .

# Use only full path name for the directories bindir, libdir, man1dir !
# Common prefix for installation directories.
# NOTE: this directory must exist when you start installation.
prefix=/usr/local

# The directory for installation of `m2c'.
bindir=$(prefix)/bin

# The directory for installation of Modula-2 run time library and 
# definition, implementation standard modules and its object files.
libdir=$(prefix)/m2lib

# The include file directory, for the m2lib.h header
includedir=$(prefix)/include

# The directory used by `m2c' for storing temporary files.
tempdir=/tmp

# The directory for installation of `m2c.1'.
man1dir=$(prefix)/man/man1

# The name of Modula-2 run time library.
m2library=m2lib.a

# C compiler and its flag used for compilation of C files.
CC=gcc
CFLAGS= -O -g -I. -I$(srcdir) -I$(srcdir)/config\
 -DSTANDARD_LIBRARY_DIRECTORY='"$(libdir)"'\
 -DTEMPORARY_DIRECTORY='"$(tempdir)"'\
 -DM2_RUN_TIME_LIBRARY='"$(m2library)"'

# Utility for convertion of archives to random libraries.
RANLIB=ranlib

# Utility for installation `m2c'.
INSTALL=install -c

# Utility for installation files into libdir.
INSTALLDATA=cp

# Utility for creation of `m2c' tag table.
ETAGS=etags

# Modula-2 translator and its flags used for creation object files
# of standard modules.
M2C=./m2c
M2CFLAGS= -O -update -c -P$(srcdir) -I$(srcdir)

# Standard definition modules.
DEFF = $(srcdir)/ASCII.def $(srcdir)/Files.def $(srcdir)/InOut.def\
       $(srcdir)/MathLib0.def $(srcdir)/NumConv.def $(srcdir)/RealConv.def\
       $(srcdir)/RealInOut.def $(srcdir)/ShellVars.def $(srcdir)/Storage.def\
       $(srcdir)/String.def $(srcdir)/Terminal.def

# Standard implementation modules.
IMPF = $(srcdir)/ASCII.mod $(srcdir)/Files.mod $(srcdir)/InOut.mod\
       $(srcdir)/MathLib0.mod $(srcdir)/NumConv.mod $(srcdir)/RealConv.mod\
       $(srcdir)/RealInOut.mod $(srcdir)/ShellVars.mod $(srcdir)/Storage.mod\
       $(srcdir)/String.mod $(srcdir)/Terminal.mod

# Distribution header files used all source files of the translator `m2c'.
COMMONDISTF=$(srcdir)/m2-common.h $(srcdir)/m2-errors.h\
            $(srcdir)/m2-icode.h $(srcdir)/m2-type-size.h\
	    $(srcdir)/m2-library.h

# All header files used all source files of the translator `m2c' .
COMMON=$(COMMONDISTF) m2-config.h

# Distribution source files of the translator `m2c'.
M2CDISTSF=$(srcdir)/m2-errors.c $(srcdir)/m2-main.c $(srcdir)/m2-icode.c\
 $(srcdir)/m2-library.c $(srcdir)/m2-type-size.c $(srcdir)/m2-scanner.c\
 $(srcdir)/m2-syntax.c $(srcdir)/m2-semantics.c $(srcdir)/m2-generator.c\
 $(COMMONDISTF) $(srcdir)/m2-syntax.h $(srcdir)/m2-semantics.h\
 $(srcdir)/m2-generator.h $(srcdir)/m2-scanner.h

# All source files of the translator `m2c'.
M2CSF=$(M2CDISTSF) m2-config.h

# Source files of run-time functions.
M2LIBSF= $(srcdir)/m2l_setin.c $(srcdir)/m2l_nites.c\
         $(srcdir)/m2l_eq.c $(srcdir)/m2l_ne.c $(srcdir)/m2l_assarr.c\
         $(srcdir)/m2l_assstr.c $(srcdir)/m2l_cap.c $(srcdir)/m2l_halt.c\
         $(srcdir)/m2l_arrpar.c $(srcdir)/m2l_testptr.c $(srcdir)/m2l_rngovf.c\
         $(srcdir)/m2l_cor.c $(srcdir)/m2lib.h

# ALL distribution files in source directory .
DISTSF = $(M2CDISTSF) $(M2LIBSF) $(DEFF) $(IMPF) $(srcdir)/Makefile.tmpl\
         $(srcdir)/configure $(srcdir)/config.sub\
	 $(srcdir)/m2c.1 $(srcdir)/COPYING\
         $(srcdir)/ChangeLog $(srcdir)/INSTALL $(srcdir)/MACHINES \
         $(srcdir)/PROJECTS $(srcdir)/README

# Subdirectories of source directory that contain other distribution files.
ADDITIONAL_DIRECTORIES= $(srcdir)/config $(srcdir)/m2-tests $(srcdir)/doc\
                        $(srcdir)/m2-examples

# Object files of the translator `m2c'.
M2F= m2-errors.o m2-main.o m2-icode.o m2-library.o m2-type-size.o\
	     m2-scanner.o m2-syntax.o m2-semantics.o m2-generator.o 

# Assembler run-time functions for coroutine implementation.
M2ASSCOR=

# All object files of the run-time library.
M2LIBPROC=$(M2ASSCOR) m2l_setin.o m2l_nites.o m2l_eq.o m2l_ne.o m2l_assarr.o\
	  m2l_assstr.o m2l_cap.o  m2l_halt.o m2l_arrpar.o m2l_testptr.o\
	  m2l_rngovf.o m2l_cor.o


# Creation of all object and executable files;
all: m2c $(m2library)
	$(M2C) $(M2CFLAGS) $(IMPF)

m2c: $(M2F)
	$(CC) -o m2c $(CFLAGS) $(M2F)

m2-errors.o: $(COMMON) $(srcdir)/m2-errors.c
	$(CC) $(CFLAGS) -c $(srcdir)/m2-errors.c
m2-main.o: $(COMMON) $(srcdir)/m2-syntax.h $(srcdir)/m2-semantics.h\
        $(srcdir)/m2-generator.h $(srcdir)/m2-main.c
	$(CC) $(CFLAGS) -c $(srcdir)/m2-main.c
m2-icode.o: $(COMMON) $(srcdir)/m2-icode.c
	$(CC) $(CFLAGS) -c $(srcdir)/m2-icode.c
m2-library.o: $(COMMON) $(srcdir)/m2-library.c
	$(CC) $(CFLAGS) -c $(srcdir)/m2-library.c
m2-type-size.o: $(COMMON) $(srcdir)/m2-type-size.c
	$(CC) $(CFLAGS) -c $(srcdir)/m2-type-size.c
m2-scanner.o: $(COMMON) $(srcdir)/m2-scanner.h $(srcdir)/m2-scanner.c
	$(CC) $(CFLAGS) -c $(srcdir)/m2-scanner.c
m2-syntax.o: $(COMMON) $(srcdir)/m2-scanner.h $(srcdir)/m2-syntax.h\
             $(srcdir)/m2-syntax.c
	$(CC) $(CFLAGS) -c $(srcdir)/m2-syntax.c
m2-semantics.o: $(COMMON) $(srcdir)/m2-semantics.h $(srcdir)/m2-semantics.c
	$(CC) $(CFLAGS) -c $(srcdir)/m2-semantics.c
m2-generator.o: $(COMMON) $(srcdir)/m2-generator.h $(srcdir)/m2-generator.c
	$(CC) $(CFLAGS) -c $(srcdir)/m2-generator.c

m2l_eq.o: m2lib.h $(srcdir)/m2l_eq.c
	$(CC) $(CFLAGS) -c $(srcdir)/m2l_eq.c
m2l_ne.o: m2lib.h $(srcdir)/m2l_ne.c
	$(CC) $(CFLAGS) -c $(srcdir)/m2l_ne.c
m2l_assarr.o: m2lib.h $(srcdir)/m2l_assarr.c
	$(CC) $(CFLAGS) -c $(srcdir)/m2l_assarr.c
m2l_assstr.o: m2lib.h $(srcdir)/m2l_assstr.c
	$(CC) $(CFLAGS) -c $(srcdir)/m2l_assstr.c
m2l_cap.o: m2lib.h $(srcdir)/m2l_cap.c
	$(CC) $(CFLAGS) -c $(srcdir)/m2l_cap.c
m2l_halt.o: m2lib.h $(srcdir)/m2l_halt.c
	$(CC) $(CFLAGS) -c $(srcdir)/m2l_halt.c
m2l_arrpar.o: m2lib.h $(srcdir)/m2l_arrpar.c
	$(CC) $(CFLAGS) -c $(srcdir)/m2l_arrpar.c
m2l_testptr.o: m2lib.h $(srcdir)/m2l_testptr.c
	$(CC) $(CFLAGS) -c $(srcdir)/m2l_testptr.c
m2l_rngovf.o: m2lib.h $(srcdir)/m2l_rngovf.c
	$(CC) $(CFLAGS) -c $(srcdir)/m2l_rngovf.c
m2l_cor.o: m2lib.h $(srcdir)/m2l_cor.c
	$(CC) $(CFLAGS) -c $(srcdir)/m2l_cor.c
m2l_setin.o: m2lib.h $(srcdir)/m2l_setin.c
	$(CC) $(CFLAGS) -c $(srcdir)/m2l_setin.c
m2l_nites.o: m2lib.h $(srcdir)/m2l_nites.c
	$(CC) $(CFLAGS) -c $(srcdir)/m2l_nites.c

$(m2library): $(M2LIBPROC)
	rm -f $(m2library)
	ar rc $(m2library) $(M2LIBPROC)

# Creation of all object files and copying the translator
# `m2c', `m2c.1', Modula-2 run time library, definition, implementation
# standard modules and its object files to target directories.
install: all uninstall $(libdir) $(bindir) $(man1dir)\
         $(libdir)/$(m2library) $(bindir)/m2c $(man1dir)/m2c.1
	$(INSTALLDATA) $(IMPF) $(DEFF) $(libdir)
	$(INSTALLDATA) m2lib.h $(includedir)
	for i in $(IMPF); do\
         $(INSTALLDATA) `basename $$i .mod`.o\
            $(libdir)/$i`basename $$i .mod`.o;\
        done

# Delete the installed files and empty installation directories.
uninstall:
	-rm -f $(libdir)/$(m2library) $(bindir)/m2c $(man1dir)/m2c.1
	-for i in $(DEFF); do\
          rm -f $(libdir)/`basename $$i`;\
        done
	-for i in $(IMPF); do\
          rm -f $(libdir)/`basename $$i`;\
          rm -f $(libdir)/`basename $$i .mod`.o;\
        done
	-rmdir $(libdir) $(bindir) $(man1dir)

$(libdir):
	mkdir $(libdir)

$(bindir):
	mkdir $(bindir)

$(man1dir):
	mkdir $(man1dir)

$(libdir)/$(m2library): $(m2library)
	$(INSTALLDATA) $(m2library) $(libdir)/$(m2library)
	$(RANLIB) $(libdir)/$(m2library)

$(bindir)/m2c: m2c
	$(INSTALL) m2c $(bindir)/m2c

$(man1dir)/m2c.1:
	$(INSTALLDATA) $(srcdir)/m2c.1 $(man1dir)/m2c.1

clean: modclean
	rm -f $(M2F) m2c $(M2LIBPROC) $(m2library)

distclean: clean
	rm -f config.status m2l_ascor.c m2-config.h Makefile
	rm -f TAGS

# Updating TAGS table for the `m2c' sources and run-time function sources.
TAGS: $(M2CSF) $(M2LIBSF)
	$(ETAGS) $(M2CSF) $(M2LIBSF)

# Unconditional creation of compressed distribution tar file.
dist:
	-mkdir $(distdir)
	rm -f -r $(distdir)/*
	cp $(DISTSF) $(distdir)
	-for i in $(ADDITIONAL_DIRECTORIES); do\
	 mkdir $(distdir)/`basename $$i`;\
	 cp $$i/* $(distdir)/`basename $$i`;\
        done
	tar cf -  $(distdir) | gzip -c >$(distdir).tar.gz 

# Deletion of object files of standard modules.
modclean:
	for i in $(IMPF); do rm -f `basename $$i .mod`.o; done
