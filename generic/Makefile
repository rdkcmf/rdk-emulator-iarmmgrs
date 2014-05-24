# List of Libraries
install_dir := ../install/bin
install_lib_dir := ../install/lib

# List of Executable
exe_ir              := ir/
exe_power           := power/
exe_sysmgr          := sysmgr/
exe_diskmgr         := disk/
exe_mfr             := mfr/
exe_ds              := dsmgr/
exe_tr69Bus         := tr69Bus/
exe_test            := test
exe_platform_ir     := ../soc/${PLATFORM_SOC}/ir
exe_platform_power  := ../soc/${PLATFORM_SOC}/power
exe_platform_fp     := ../soc/${PLATFORM_SOC}/fp


#executable := $(exe_platform_ir) $(exe_platform_power) $(exe_platform_fp) $(exe_ir) $(exe_power) $(exe_diskmgr) $(exe_sysmgr) $(exe_tr69Bus) $(exe_test) $(exe_mfr) $(exe_ds)
executable := 

.PHONY: clean all $(executable) install

all: clean $(executable) install 

$(executable):
	$(MAKE) -C $@

install:
	echo "Creating directory.."
	mkdir -p $(install_dir)
	mkdir -p $(install_lib_dir)
	echo "Copying files now.."	
#	cp $(exe_diskmgr)/*Main $(install_dir)
#	cp $(exe_sysmgr)/*Main $(install_dir)
#	cp $(exe_power)/*Main $(install_dir)
#	cp $(exe_ir)/*Main $(install_dir)
ifneq ($(PLATFORM_SOC),entropic)
#	cp $(exe_platform_ir)/*.so $(install_lib_dir)
endif
#	cp $(exe_ds)/*Main $(install_dir)
#	cp $(exe_tr69Bus)/*Main $(install_dir)
ifeq ($(COMCAST_PLATFORM), XI3)
#	cp $(exe_mfr)/*Main $(install_dir)
#		cp $(exe_test)/mfr_deletePDRI $(install_dir)
#		cp $(exe_test)/mfr_scrubAllBanks $(install_dir)
endif
ifeq ($(PLATFORM_SOC),intel)
#	cp $(exe_diskmgr)/*Main $(install_dir)
#	cp $(exe_ds)/*Main $(install_dir)
endif
clean:
	rm -rf $(install_dir)
	rm -rf $(install_lib_dir)
	

