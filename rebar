### makefile4rebar bootrater

define bootstrap
cd .. ; \
dir=`pwd` ; \
cd makefile4rebar ; \
if [ "`basename $$dir`" != "deps" ] ; then \
	answer=qoopa ; \
	while [ "$$answer" != "y" -a "$$answer" != "n" ] ; do \
		echo Are you positive that $$dir is THE 'deps' directory \[y/n\]? ; \
		read answer ; \
	done ; \
	if [ "$$answer" != "y" ] ; then \
		echo So, I cannot bootstrap makefile4rebar. Quitting. ; \
		exit 1 ; \
	fi ; \
fi ; \
if [ -f ../../Makefile ] ; then \
	cp ../../Makefile ../../Makefile.`date +"%Y%m%d%H%M%s"` ; \
fi ; \
cp makefile4rebar ../../Makefile
endef

all: bootstrap

bootstrap:
	@$(bootstrap)
