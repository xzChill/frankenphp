PHP_PATH=C:/msys64-new/usr/local/include/php
INCLUDES=-I$(PHP_PATH) -I$(PHP_PATH)/main -I$(PHP_PATH)/TSRM -I$(PHP_PATH)/Zend -I$(PHP_PATH)/ext
MACROS=-D_WINDOWS -DWINDOWS=1 -DZEND_WIN32=1 -DPHP_WIN32=1 -DWIN32 -D_MBCS -D_USE_MATH_DEFINES -DNDebug -DNDEBUG -DZEND_DEBUG=0 -DZTS=1 -DFD_SETSIZE=256
GCCMACROS=-D_POSIX
CGOCFLAGS=$(INCLUDES) $(MACROS) $(GCCMACROS)
LDPATH=-LC:/msys64-new/usr/local/lib
CGOLDFLAGS=$(LDPATH) -lphp8ts -lphp8embed -lbrotlicommon -lbrotlidec -lbrotlienc

build:
	CGO_CFLAGS="$(CGOCFLAGS)" CGO_LDFLAGS="$(CGOLDFLAGS)" go build -a -x

clean:
	rm -r *.exe