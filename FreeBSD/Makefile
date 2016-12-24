#################################################################
# Installing Openbox-Enhanced-Menu, to appropriate directories.	#
# Author: Geovani Barzaga Rodriguez <igeo.cu@gmail.com>.	#
# Openbox-Enhanced-Menu 2016. BSD License.			#
#################################################################

PREFIXbin=$(RPM_BUILD_ROOT)/home/${USER}/bin
PREFIXopenbox=$(RPM_BUILD_ROOT)/home/${USER}/.config/openbox

install:
	mkdir -p $(PREFIXbin)
	mkdir -p $(PREFIXopenbox)
	cp bin/* $(PREFIXbin)
	cp -R openbox/* $(PREFIXopenbox)
	$(PREFIXbin)/ob-menu-regenerator

uninstall:
	rm -f $(PREFIXbin)/ob-menu-regenerator
	rm -rf $(PREFIXopenbox)/*
	openbox --reconfigure
