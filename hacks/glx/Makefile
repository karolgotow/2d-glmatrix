# hacks/glx/Makefile.in --- xscreensaver, Copyright (c) 1999-2018
#  by Jamie Zawinski.
# the `../../configure' script generates `hacks/glx/Makefile' from this file.


.SUFFIXES:
.SUFFIXES: .c .o

srcdir		= .

top_srcdir	= ../..
top_builddir	= ..

install_prefix	=
prefix		= /usr/local
exec_prefix	= ${prefix}
bindir		= ${exec_prefix}/bin
datarootdir	= ${prefix}/share
datadir		= ${datarootdir}
mandir		= ${datarootdir}/man
libexecdir	= ${exec_prefix}/libexec
mansuffix	= 6
manNdir		= $(mandir)/man$(mansuffix)

HACKDIR		= ${libexecdir}/xscreensaver
HACK_CONF_DIR	= ${datadir}/xscreensaver/config

CC		= gcc -pedantic -Wall -Wstrict-prototypes -Wnested-externs -Wmissing-prototypes -Wno-overlength-strings -Wdeclaration-after-statement -std=c89 -U__STRICT_ANSI__
CFLAGS		= -g -O2
LDFLAGS		=  -L${exec_prefix}/lib
DEFS		= -DSTANDALONE -DUSE_GL -DHAVE_CONFIG_H
LIBS		= 
PERL		= /usr/bin/perl

DEPEND		= makedepend
DEPEND_FLAGS	= 
DEPEND_DEFINES	= 

SHELL		= /bin/sh
INSTALL		= /usr/bin/install -c
SUID_FLAGS      = -o root -m 4755
INSTALL_PROGRAM = ${INSTALL}
INSTALL_SETUID  = $(INSTALL_PROGRAM) $(SUID_FLAGS)
INSTALL_DATA	= ${INSTALL} -m 644
INSTALL_DIRS	= ${INSTALL} -d
PROG_SETCAP	= 
SETCAP_FLAGS	= cap_net_raw=p

X_CFLAGS	= 
X_LIBS		= 
X_PRE_LIBS	=  -lSM -lICE
X_EXTRA_LIBS	= 
XMU_LIBS	= 
XFT_LIBS	= -lXft

# Note: see comment in ../../driver/Makefile.in for explanation of X_LIBS, etc.
#
HACK_PRE	= $(LIBS) $(X_LIBS)
HACK_POST     = $(X_PRE_LIBS) $(XFT_LIBS) -lXt -lX11 $(XMU_LIBS) -lXext $(X_EXTRA_LIBS) -lm
HACK_POST2	= -lGL -lGLU  -lpthread  $(HACK_POST)
HACK_LIBS	= $(HACK_PRE)            $(HACK_POST2)
PNG_LIBS	= $(HACK_PRE)            -lpng $(HACK_POST2)
GLE_LIBS	= $(HACK_PRE)  -lpng $(HACK_POST2)
TEXT_LIBS	= -lutil
#### Is LIBCAP_CFLAGS necessary?
LIBCAP_CFLAGS	= 
LIBCAP_LIBS	= 

HACK_SRC	= $(srcdir)/..
HACK_BIN	= ..
UTILS_SRC	= $(HACK_SRC)/../utils
JWXYZ_SRC	= $(HACK_SRC)/../jwxyz
UTILS_BIN	= $(HACK_BIN)/../utils
JWXYZ_BIN	= $(HACK_BIN)/../jwxyz

INCLUDES_1	= -I. -I$(srcdir) -I$(UTILS_SRC) -I$(JWXYZ_SRC) -I$(HACK_SRC) -I$(HACK_BIN) -I../..
INCLUDES	= $(INCLUDES_1)  -I/usr/include/uuid -I/usr/include/freetype2 -I/usr/include/libpng16

UTILDIR_OBJS	= $(UTILS_BIN)/colors.o $(UTILS_BIN)/grabclient.o \
		  $(UTILS_BIN)/hsv.o $(UTILS_BIN)/resources.o \
		  $(UTILS_BIN)/usleep.o $(UTILS_BIN)/visual.o \
		  $(UTILS_BIN)/xmu.o $(UTILS_BIN)/xft.o \
		  $(UTILS_BIN)/utf8wc.o $(UTILS_BIN)/logo.o \
		  $(UTILS_BIN)/visual-gl.o \
		  $(UTILS_BIN)/yarandom.o $(UTILS_BIN)/xshm.o \
		  $(UTILS_BIN)/textclient.o $(UTILS_BIN)/async_netdb.o \
		  $(UTILS_BIN)/aligned_malloc.o $(UTILS_BIN)/thread_util.o \
		  $(UTILS_BIN)/spline.o $(UTILS_BIN)/pow2.o \
		  $(UTILS_SRC)/font-retry.c
JWXYZ_OBJS	= $(JWXYZ_BIN)/jwzgles.o
HACKDIR_OBJS	= $(HACK_BIN)/screenhack.o $(HACK_BIN)/xlockmore.o \
		  $(HACK_BIN)/fps.o $(HACK_BIN)/ximage-loader.o
PNG		= $(HACK_BIN)/ximage-loader.o

SRCS		= glmatrix.c

OBJS		= 

GL_EXES		= glmatrix
GLE_EXES	= extrusion
SUID_EXES	= 
SETCAP_EXES	= 
GL_UTIL_EXES	= xscreensaver-gl-helper
JWZGLES_OBJS	= 
HACK_EXES_1	= $(GL_EXES) 
HACK_EXES	= $(HACK_EXES_1) $(SUID_EXES)
XSHM_OBJS	= $(UTILS_BIN)/xshm.o
GRAB_OBJS	= $(UTILS_BIN)/grabclient.o grab-ximage.o $(XSHM_OBJS)
ANIM_OBJS	= recanim-gl.o
ANIM_LIBS	= -lpng
EXES		= $(GL_UTIL_EXES) $(HACK_EXES)

RETIRED_EXES	= $(RETIRED_GL_EXES)
RETIRED_GL_EXES	= 

FPS_OBJS	= texfont.o $(HACK_BIN)/fps.o fps-gl.o 
HACK_OBJS	= $(JWZGLES_OBJS) $(HACK_BIN)/screenhack.o  \
		  $(HACK_BIN)/xlockmore.o xlock-gl-utils.o erase-gl.o \
		  ${FPS_OBJS} $(UTILS_BIN)/resources.o $(UTILS_BIN)/visual.o \
		  $(UTILS_BIN)/visual-gl.o $(UTILS_BIN)/usleep.o \
		  $(UTILS_BIN)/yarandom.o $(UTILS_BIN)/hsv.o \
		  $(UTILS_BIN)/colors.o $(UTILS_BIN)/async_netdb.o \
		  $(UTILS_BIN)/aligned_malloc.o $(UTILS_BIN)/thread_util.o \
		  $(UTILS_BIN)/utf8wc.o $(UTILS_BIN)/pow2.o \
		  $(UTILS_BIN)/font-retry-xft.o $(UTILS_BIN)/xmu.o

HDRS		= 
GL_MEN		= 
MEN		= $(GL_MEN)
RETIRED_MEN	= glforestfire.man
EXTRAS		= README Makefile.in dxf2gl.pl vrml2gl.pl wfront2gl.pl \
		  molecules.sh starwars.txt zalgo.txt *.dxf

TARFILES	= $(SRCS) $(HDRS) $(GL_MEN) $(RETIRED_MEN) $(EXTRAS)


default: all
all: $(EXES) $(RETIRED_EXES)

install:   install-program    install-xml   install-man
uninstall: uninstall-program  uninstall-xml uninstall-man

install-strip:
	$(MAKE) INSTALL_PROGRAM='$(INSTALL_PROGRAM) -s' install

# the hacks, in $HACKDIR
install-program:: $(EXES)
	@exes="$(HACK_EXES_1)" ;					\
	 idir="$(install_prefix)$(HACKDIR)" ;				\
	 if [ "$$exes" != "" ]; then					\
	   if [ ! -d $$idir ]; then					\
	     $(INSTALL_DIRS) $$idir ;					\
	   fi ;								\
	   for program in $$exes; do					\
	     echo $(INSTALL_PROGRAM) $$program $$idir/$$program ;	\
		  $(INSTALL_PROGRAM) $$program $$idir/$$program ;	\
	   done ;							\
									\
	   exes="$(SUID_EXES)" ;					\
	   if [ yes = yes ]; then				\
	     sinst="$(INSTALL_SETUID)" ;				\
	   else								\
	     sinst="$(INSTALL_PROGRAM)" ;				\
	   fi ;								\
	   for program in $$exes; do					\
	     echo $$sinst $$program $$idir/$$program ;			\
	     if   $$sinst $$program $$idir/$$program ; then		\
	        true ;							\
	     elif [ yes = yes ]; then			\
	       echo $(INSTALL_PROGRAM) $$program $$idir/$$program ;	\
	       if   $(INSTALL_PROGRAM) $$program $$idir/$$program ; then\
	         echo "" ;						\
	         echo "WARNING: unable to install $$program setuid:"	\
	              "installed non-setuid instead." ;			\
	         echo "" ;						\
	       else							\
	         exit 1 ;						\
	       fi ;							\
	     else							\
	       exit 1 ;							\
	     fi ;							\
	   done ;							\
									\
	   exes="${SETCAP_EXES}" ;					\
	   if [ no = yes ]; then				\
	     for program in $$exes; do					\
	       echo $(PROG_SETCAP) $(SETCAP_FLAGS) $$idir/$$program ;	\
	       if   $(PROG_SETCAP) $(SETCAP_FLAGS) $$idir/$$program ; then \
	         true ;							\
	       else							\
	         echo "" ;						\
	         echo "WARNING: unable to setcap $$program" ;		\
	         echo "" ;						\
	       fi ;							\
	     done ;							\
	   fi ;								\
	 fi


# the xscreensaver-gl-helper program, in $bindir
install-program:: $(EXES)
	@exes="$(GL_UTIL_EXES)" ;					\
	 idir="$(install_prefix)$(bindir)" ;				\
	 if [ "$$exes" != "" ]; then					\
	   if [ ! -d $$idir ]; then					\
	     $(INSTALL_DIRS) $$idir ;					\
	   fi ;								\
	   for program in $$exes; do					\
	     echo $(INSTALL_PROGRAM) $$program $$idir/$$program ;	\
		  $(INSTALL_PROGRAM) $$program $$idir/$$program ;	\
	   done ;							\
	 fi

# When installing man pages, we install "foo.man" as "foo.N" and update
# the .TH line in the installed file with one like
#
#     .TH XScreenSaver N "V.VV (DD-MMM-YYYY)" "X Version 11"
#
# where N is the manual section suffix.
#
install-man: $(MEN)
	@men="$(MEN)" ;							\
	U=$(UTILS_SRC)/version.h ;					\
	V=`sed -n 's/.*xscreensaver \([0-9]\.[^)]*)\).*/\1/p' < $$U` ;	\
	T=/tmp/xs$$$$.$(mansuffix) ;					\
	TH=".TH XScreenSaver $(mansuffix) \"$$V\" \"X Version 11\"" ;	\
	echo "installing man pages: $$TH" ;				\
									\
	if [ ! -d $(install_prefix)$(manNdir) ]; then			\
	  $(INSTALL_DIRS) $(install_prefix)$(manNdir) ;			\
	 fi ;								\
									\
	for man in $$men; do						\
	  instname=`echo $$man | sed 's/\.man$$/\.$(mansuffix)/'` ;	\
	  manbase=`echo $$man | sed 's/\.man$$//'` ;    \
	  TH=".TH $$manbase $(mansuffix) \"$$V\" \"X Version 11\" \"XScreenSaver manual\"" ;   \
	  sed -e "s/^\.TH.*/$$TH/"					\
	      -e 's@(MANSUFFIX)@($(mansuffix))@g'			\
	    < $(srcdir)/$$man > $$T ;					\
	  echo $(INSTALL_DATA) $(srcdir)/$$man				\
	   $(install_prefix)$(manNdir)/$$instname ;			\
	  $(INSTALL_DATA) $$T						\
	    $(install_prefix)$(manNdir)/$$instname ;			\
	done ;								\
	rm -f $$T

install-xml:
	@dest=$(install_prefix)$(HACK_CONF_DIR) ;			\
	 if [ ! -d $$dest ]; then					\
	   $(INSTALL_DIRS) $$dest ;					\
	 fi ;								\
	 src=$(srcdir)/../config ;					\
	 for file in $(EXES) $(SCRIPTS) ; do				\
	   if [ -f $$src/$$file.xml ]; then				\
	     echo $(INSTALL_DATA) $$src/$$file.xml $$dest/$$file.xml ;	\
	          $(INSTALL_DATA) $$src/$$file.xml $$dest/$$file.xml ;	\
	   fi ;								\
	done

# the hacks, in $HACKDIR
uninstall-program::
	@exes="$(HACK_EXES) $(RETIRED_EXES)" ;				\
	 idir="$(install_prefix)$(HACKDIR)" ;				\
	 for program in $$exes; do					\
	   echo rm -f $$idir/$$program ;				\
		rm -f $$idir/$$program ;				\
	 done

# the xscreensaver-gl-helper program, in $bindir
uninstall-program::
	@exes="$(GL_UTIL_EXES)" ;					\
	 idir="$(install_prefix)$(bindir)" ;				\
	 for program in $$exes; do					\
	   echo rm -f $$idir/$$program ;				\
		rm -f $$idir/$$program ;				\
	done

uninstall-man:
	@men="$(MEN) $(RETIRED_MEN)" ;					\
	for man in $$men; do						\
	  instname=`echo $$man | sed 's/\.man$$/\.$(mansuffix)/'` ;	\
	  echo rm -f $(install_prefix)$(manNdir)/$$instname* ;		\
	       rm -f $(install_prefix)$(manNdir)/$$instname* ;		\
	done

uninstall-xml:
	@dest=$(install_prefix)$(HACK_CONF_DIR) ;			\
	 for file in $(EXES) $(RETIRED_EXES) $(SCRIPTS) ; do		\
	     echo rm -f $$dest/$$file.xml ;				\
	          rm -f $$dest/$$file.xml ;				\
	done

clean::
	-rm -f *.o a.out core $(EXES) $(RETIRED_EXES) molecules.h

distclean: clean
	-rm -f Makefile TAGS *~ "#"*

# Adds all current dependencies to Makefile
depend:
	$(DEPEND) -s '# DO NOT DELETE: updated by make depend'		    \
	$(DEPEND_FLAGS) --						    \
	$(INCLUDES) $(DEFS) $(DEPEND_DEFINES) $(CFLAGS) $(X_CFLAGS) --	    \
	$(SRCS)

# Adds some dependencies to Makefile.in -- not totally accurate, but pretty
# close.  This excludes dependencies on files in /usr/include, etc.  It tries
# to include only dependencies on files which are themselves a part of this
# package.
distdepend:: molecules.h
	@echo updating dependencies in `pwd`/Makefile.in... ;		    \
	$(DEPEND) -w 0 -f - 						    \
	-s '# DO NOT DELETE: updated by make distdepend' $(DEPEND_FLAGS) -- \
	$(INCLUDES_1) $(DEFS) $(DEPEND_DEFINES) $(CFLAGS) $(X_CFLAGS) --    \
	$(SRCS) 2>/dev/null |						    \
	sort -d |							    \
	(								    \
	  awk '/^# .*Makefile.in ---/,/^# DO .*distdepend/' < Makefile.in ; \
	  sed -e '/^#.*/d'						    \
	      -e 's@ \./@ @g;s@ /[^ ]*@@g;/^.*:$$/d'			    \
	      -e 's@\.\./\.\./utils@$$(UTILS_SRC)@g'			    \
	      -e 's@\.\./\.\./jwxyz@$$(JWXYZ_SRC)@g'			    \
	      -e 's@\.\./glx/@@g'					    \
	      -e 's@ \.\./@ $$(HACK_SRC)/@g'				    \
	      -e 's@ \([^$$]\)@ $$(srcdir)/\1@g'			    \
	      -e 's@ $$(srcdir)/\(.*config.h\)@ \1@g'			    \
	      -e 's@ $$(HACK_SRC)/\(.*config.h\)@ ../\1@g'		    \
	      -e 's@ $$(srcdir)/\(.*molecules.h\)@ \1@g'		    \
	      -e 's@ $$(srcdir)/\(images/gen/\)@ ../\1@g'		    \
	      -e 's@ $$(HACK_SRC)/\(images/gen/\)@ ../\1@g' ;		    \
	  echo ''							    \
	) > /tmp/distdepend.$$$$ &&					    \
	mv /tmp/distdepend.$$$$ Makefile.in


TAGS: tags
tags:
	find $(srcdir) -name '*.[chly]' -print | xargs etags -a

echo_tarfiles:
	@echo $(TARFILES)

check_men:
	@badmen="" ;							\
	 for exe in $(EXES); do						\
	   if ! [ -f $(srcdir)/$$exe.man ]; then			\
	     badmen="$$badmen $$exe" ;					\
	   fi ;								\
	 done ;								\
	 if [ -n "$$badmen" ]; then					\
	   echo "" ;							\
	   echo "Warning: The following programs have no manuals:" ;	\
	   echo "" ;							\
	   for m in $$badmen ; do					\
	     echo "    $$m" ;						\
	   done ;							\
	 fi

validate_xml:
	@echo "Validating XML..." ; \
	cd $(HACK_SRC) ; ./check-configs.pl $(GL_EXES) $(GLE_EXES) $(SUID_EXES)

distdepend:: check_men validate_xml



# Rules for noticing when the objects from the utils and hacks
# directories are out of date with respect to their sources, and going
# and building them according to the rules in their own Makefile...
#
$(UTILS_BIN)/colors.o:		$(UTILS_SRC)/colors.c
$(UTILS_BIN)/grabclient.o:	$(UTILS_SRC)/grabclient.c
$(UTILS_BIN)/hsv.o:		$(UTILS_SRC)/hsv.c
$(UTILS_BIN)/resources.o:	$(UTILS_SRC)/resources.c
$(UTILS_BIN)/usleep.o:		$(UTILS_SRC)/usleep.c
$(UTILS_BIN)/visual.o:		$(UTILS_SRC)/visual.c
$(UTILS_BIN)/xmu.o:		$(UTILS_SRC)/xmu.c
$(UTILS_BIN)/xft.o:		$(UTILS_SRC)/xft.c
$(UTILS_BIN)/utf8wc.o:		$(UTILS_SRC)/utf8wc.c
$(UTILS_BIN)/logo.o:		$(UTILS_SRC)/logo.c
$(UTILS_BIN)/visual-gl.o:	$(UTILS_SRC)/visual-gl.c
$(UTILS_BIN)/yarandom.o:	$(UTILS_SRC)/yarandom.c
$(UTILS_BIN)/xshm.o:		$(UTILS_SRC)/xshm.c
$(UTILS_BIN)/textclient.o:	$(UTILS_SRC)/textclient.c
$(UTILS_BIN)/async_netdb.o:	$(UTILS_SRC)/async_netdb.c
$(UTILS_BIN)/aligned_malloc.o:	$(UTILS_SRC)/aligned_malloc.c
$(UTILS_BIN)/thread_util.o:	$(UTILS_SRC)/thread_util.c
$(UTILS_BIN)/spline.o:		$(UTILS_SRC)/spline.c
$(UTILS_BIN)/pow2.o:		$(UTILS_SRC)/pow2.c
$(UTILS_BIN)/font-retry-xft.o:	$(UTILS_SRC)/font-retry.c
$(HACK_BIN)/screenhack.o:	$(HACK_SRC)/screenhack.c
$(HACK_BIN)/xlockmore.o:	$(HACK_SRC)/xlockmore.c
$(HACK_BIN)/fps.o:		$(HACK_SRC)/fps.c

$(UTILDIR_OBJS):
	cd $(UTILS_BIN) ; $(MAKE) $(@F) CC="$(CC)" CFLAGS="$(CFLAGS)"
$(JWXYZ_OBJS):
	cd $(JWXYZ_BIN) ; $(MAKE) $(@F) CC="$(CC)" CFLAGS="$(CFLAGS)"
$(HACKDIR_OBJS):
	cd $(HACK_BIN)  ; $(MAKE) $(@F) CC="$(CC)" CFLAGS="$(CFLAGS)"


# How we build object files in this directory.
.c.o:
	$(CC) -c $(INCLUDES) $(DEFS) $(CPPFLAGS) $(CFLAGS) $(X_CFLAGS) $<

# Make sure the images have been packaged. This is the first one hit:
../images/gen/wood_png.h:
	cd ../images && $(MAKE)

# How to build the "xscreensaver-gl-helper" program, that lets the daemon
# know which visual is the right one for GL programs.
#
GLH1=xscreensaver-gl-helper.o $(UTILS_BIN)/visual-gl.o
GLH2=$(UTILS_BIN)/visual.o $(UTILS_BIN)/resources.o
xscreensaver-gl-helper:        $(GLH1) $(GLH2)
	$(CC) $(LDFLAGS) -o $@ $(GLH1) $(GLH2) $(LIBS) $(X_LIBS) $(HACK_POST2)


# These hacks use a slightly-differently-compiled variant of recanim.c.
# This is how to make the the other .o file from it.
#
XLM_CFLAGS=-DUSE_GL $(INCLUDES) $(DEFS) $(CPPFLAGS) $(CFLAGS) $(X_CFLAGS)
recanim-gl.o: $(HACK_SRC)/recanim.c
	$(CC) -o $@ -c $(XLM_CFLAGS) $(HACK_SRC)/recanim.c

CC_HACK		= $(CC) $(LDFLAGS)


TRACK_OBJS=rotator.o trackball.o gltrackball.o
HACK_TRACK_OBJS=$(HACK_OBJS) $(TRACK_OBJS)
HACK_GRAB_OBJS=$(HACK_OBJS) $(GRAB_OBJS)
HACK_TRACK_GRAB_OBJS=$(HACK_TRACK_OBJS) $(GRAB_OBJS)
HACK_GLSL_OBJS=$(HACK_TRACK_OBJS) glsl_support.o
TEXT=$(UTILS_BIN)/textclient.o

ATLANTIS_OBJS = $(HACK_OBJS) dolphin.o shark.o swim.o whale.o $(PNG)

glmatrix:	glmatrix.o	$(PNG) $(HACK_OBJS)
	$(CC_HACK) -o $@ $@.o	$(PNG) $(HACK_OBJS) $(PNG_LIBS)



##############################################################################
#
# DO NOT DELETE: updated by make distdepend


glmatrix.o: ../../config.h
glmatrix.o: $(HACK_SRC)/fps.h
glmatrix.o: ../images/gen/matrix3_png.h
glmatrix.o: $(HACK_SRC)/recanim.h
glmatrix.o: $(HACK_SRC)/screenhackI.h
glmatrix.o: $(UTILS_SRC)/colors.h
glmatrix.o: $(UTILS_SRC)/erase.h
glmatrix.o: $(UTILS_SRC)/font-retry.h
glmatrix.o: $(UTILS_SRC)/grabscreen.h
glmatrix.o: $(UTILS_SRC)/hsv.h
glmatrix.o: $(UTILS_SRC)/resources.h
glmatrix.o: $(UTILS_SRC)/usleep.h
glmatrix.o: $(UTILS_SRC)/visual.h
glmatrix.o: $(UTILS_SRC)/yarandom.h
glmatrix.o: $(HACK_SRC)/ximage-loader.h
glmatrix.o: $(HACK_SRC)/xlockmoreI.h
glmatrix.o: $(HACK_SRC)/xlockmore.h


