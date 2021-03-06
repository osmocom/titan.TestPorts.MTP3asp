# This Makefile was generated by the compiler
# of the TTCN-3 Test Executor version 1.4.pl3
# for Attila Balasko (ethbaat@duna199) on Mon Sep 15 15:48:45 2003

# The following make commands are available:
# - make, make all       Builds the executable test suite.
# - make compile         Translates TTCN-3 and ASN.1 modules to C++.
# - make clean           Removes all generated files.
# - make dep             Creates/updates dependency list.
# - make archive         Archives all source files.

#
# Set these variables...
#

# The path of your TTCN-3 Test Executor installation:
# Uncomment this line to override the environment variable.
# TTCN3_DIR =

# Your platform: (SOLARIS, LINUX, FREEBSD or WIN32)
PLATFORM = SOLARIS8

# Your C++ compiler:
CXX = g++

# Flags for the C++ preprocessor (and makedepend as well):
CPPFLAGS = -D$(PLATFORM) -I$(TTCN3_DIR)/include -I$(SEA_DIR)/include

# Flags for the C++ compiler:
CXXFLAGS = -Wall

# Flags for the linker:
LDFLAGS =

# Flags for the TTCN-3 and ASN.1 compiler:
COMPILER_FLAGS = -L

# Execution mode: (either ttcn3 or ttcn3-parallel)
TTCN3_LIB = ttcn3-parallel

# The path of your OpenSSL installation:
# If you do not have your own one, leave it unchanged.
OPENSSL_DIR = $(TTCN3_DIR)

# Directory to store the archived source files:
# Note: you can set any directory except ./archive
ARCHIVE_DIR = ./backup

SEA_DIR = /vobs/ttcn/TCC_Releases/Other/SEA_LATEST
#
# You may change these variables. Add your files if necessary...
#

# The TTCN-3 modules needed for this project:
TTCN3_MODULES = mtp3test.ttcn MTP3asp_Types.ttcn MTP3asp_PortType.ttcn
# The ASN.1 modules needed for this project:
ASN1_MODULES =

# C++ source & header files generated by TTCN-3 & ASN.1 compilers:
GENERATED_SOURCES = $(TTCN3_MODULES:.ttcn=.cc)
GENERATED_HEADERS = $(GENERATED_SOURCES:.cc=.hh)
# Source & header files of Test Ports and your other modules:
USER_SOURCES = MTP3asp_PT.cc
USER_HEADERS = MTP3asp_PT.hh

# All object files needed for the executable test suite:
#OBJECTS = mtp3test.o MTP3_ASPs.o general_typedefs.o MTP3user_porttype.o
OBJECTS = $(GENERATED_SOURCES:.cc=.o) $(USER_SOURCES:.cc=.o) 
# The name of the executable test suite:
TARGET = mtp3test

#The names of the config files (to archive):
TARGET_CONFIGS = mtp3test_MTP3_ansi2.cfg
#
# Do not modify these unless you know what you are doing...
#
SOLARIS_LIBS = -lxnet
LINUX_LIBS =
FREEBSD_LIBS =
WIN32_LIBS =

#
# Rules for building the executable...
#
all: $(TARGET) ;

$(TARGET): $(OBJECTS)
	$(CXX) $(LDFLAGS) -o $@ $(OBJECTS) \
        -L$(TTCN3_DIR)/lib -l$(TTCN3_LIB) \
	-L$(OPENSSL_DIR)/lib -lcrypto $($(PLATFORM)_LIBS) $(SEA_DIR)/lib/libmphclib.a -lxml2

.cc.o .c.o:
	$(CXX) -c $(CPPFLAGS) $(CXXFLAGS) $<

$(GENERATED_SOURCES) $(GENERATED_HEADERS): compile
	@if [ ! -f $@ ]; then $(RM) compile; $(MAKE) compile; fi

compile: $(TTCN3_MODULES) $(ASN1_MODULES)
	$(TTCN3_DIR)/bin/compiler $(COMPILER_FLAGS) $(TTCN3_MODULES) \
	$(ASN1_MODULES) - $?
	touch $@

clean:
	-$(RM) $(TARGET) $(OBJECTS) $(GENERATED_HEADERS) \
	$(GENERATED_SOURCES) compile *.log

dep: $(GENERATED_SOURCES)
	makedepend $(CPPFLAGS) $(USER_SOURCES) $(GENERATED_SOURCES)

archive:
	mkdir -p $(ARCHIVE_DIR)
	tar -cvhf - $(TTCN3_MODULES) $(ASN1_MODULES) \
	$(USER_HEADERS) $(USER_SOURCES) $(TARGET_CONFIGS) Makefile \
	| gzip >$(ARCHIVE_DIR)/$(TARGET)-`date '+%y%m%d-%H%M'`.tgz

#
# Add your rules here if necessary...
#

# DO NOT DELETE

MTP3asp_PT.o: /usr/include/stdio.h /usr/include/iso/stdio_iso.h
MTP3asp_PT.o: /usr/include/sys/feature_tests.h /usr/include/sys/isa_defs.h
MTP3asp_PT.o: /usr/include/sys/va_list.h /usr/include/stdio_tag.h
MTP3asp_PT.o: /usr/include/stdio_impl.h /usr/include/stdlib.h
MTP3asp_PT.o: /usr/include/iso/stdlib_iso.h /usr/include/sys/types.h
MTP3asp_PT.o: /usr/include/sys/machtypes.h /usr/include/sys/int_types.h
MTP3asp_PT.o: /usr/include/sys/select.h /usr/include/sys/time.h
MTP3asp_PT.o: /usr/include/time.h /usr/include/iso/time_iso.h
MTP3asp_PT.o: /usr/include/netinet/in.h /usr/include/sys/stream.h
MTP3asp_PT.o: /usr/include/sys/vnode.h /usr/include/sys/t_lock.h
MTP3asp_PT.o: /usr/include/sys/machlock.h /usr/include/sys/param.h
MTP3asp_PT.o: /usr/include/sys/unistd.h /usr/include/sys/mutex.h
MTP3asp_PT.o: /usr/include/sys/rwlock.h /usr/include/sys/semaphore.h
MTP3asp_PT.o: /usr/include/sys/condvar.h /usr/include/sys/time_impl.h
MTP3asp_PT.o: /usr/include/sys/cred.h /usr/include/sys/uio.h
MTP3asp_PT.o: /usr/include/sys/resource.h /usr/include/vm/seg_enum.h
MTP3asp_PT.o: /usr/include/sys/poll.h /usr/include/sys/strmdep.h
MTP3asp_PT.o: /usr/include/sys/model.h /usr/include/sys/strft.h
MTP3asp_PT.o: /usr/include/sys/byteorder.h /usr/include/netdb.h
MTP3asp_PT.o: /usr/include/sys/socket.h /usr/include/sys/netconfig.h
MTP3asp_PT.o: /usr/include/sys/un.h /usr/include/net/if_dl.h
MTP3asp_PT.o: /usr/include/sys/wait.h /usr/include/sys/siginfo.h
MTP3asp_PT.o: /usr/include/sys/machsig.h /usr/include/sys/procset.h
MTP3asp_PT.o: /usr/include/unistd.h /usr/include/arpa/inet.h
MTP3asp_PT.o: /usr/include/stdarg.h /usr/include/iso/stdarg_iso.h
MTP3asp_PT.o: /usr/include/string.h /usr/include/iso/string_iso.h
MTP3asp_PT.o: MTP3asp_PT.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/TTCN3.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/version.h
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Basetype.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Types.h
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Encdec.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Template.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Integer.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Optional.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/BER.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Logger.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Textbuf.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Error.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Parameters.h
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Float.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Boolean.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/ASN_Null.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Objid.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Verdicttype.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Component.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Bitstring.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/RAW.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Hexstring.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Octetstring.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/ASN_Any.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Charstring.hh
MTP3asp_PT.o: /usr/include/regex.h
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Universal_charstring.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Struct_of.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Array.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/ASN_CharacterString.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/ASN_External.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/ASN_EmbeddedPDV.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Addfunc.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Timer.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Port.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Module_list.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Snapshot.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Default.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Runtime.hh
MTP3asp_PT.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/TEXT.hh
MTP3asp_PT.o: /vobs/ttcn/TCC_Releases/Other/SEA_LATEST/include/mphclib.h
MTP3asp_PT.o: MTP3asp_Types.hh MTP3asp_PortType.hh
mtp3test.o: mtp3test.hh MTP3asp_PortType.hh MTP3asp_Types.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/TTCN3.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/version.h
mtp3test.o: /usr/include/string.h /usr/include/iso/string_iso.h
mtp3test.o: /usr/include/sys/feature_tests.h /usr/include/sys/isa_defs.h
mtp3test.o: /usr/include/stdio.h /usr/include/iso/stdio_iso.h
mtp3test.o: /usr/include/sys/va_list.h /usr/include/stdio_tag.h
mtp3test.o: /usr/include/stdio_impl.h
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Basetype.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Types.h
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Encdec.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Template.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Integer.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Optional.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/BER.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Logger.hh
mtp3test.o: /usr/include/stdlib.h /usr/include/iso/stdlib_iso.h
mtp3test.o: /usr/include/stdarg.h /usr/include/iso/stdarg_iso.h
mtp3test.o: /usr/include/sys/time.h /usr/include/sys/types.h
mtp3test.o: /usr/include/sys/machtypes.h /usr/include/sys/int_types.h
mtp3test.o: /usr/include/sys/select.h /usr/include/time.h
mtp3test.o: /usr/include/iso/time_iso.h
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Textbuf.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Error.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Parameters.h
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Float.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Boolean.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/ASN_Null.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Objid.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Verdicttype.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Component.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Bitstring.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/RAW.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Hexstring.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Octetstring.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/ASN_Any.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Charstring.hh
mtp3test.o: /usr/include/regex.h
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Universal_charstring.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Struct_of.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Array.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/ASN_CharacterString.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/ASN_External.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/ASN_EmbeddedPDV.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Addfunc.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Timer.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Port.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Module_list.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Snapshot.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Default.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Runtime.hh
mtp3test.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/TEXT.hh
mtp3test.o: MTP3asp_PT.hh
mtp3test.o: /vobs/ttcn/TCC_Releases/Other/SEA_LATEST/include/mphclib.h
MTP3asp_Types.o: MTP3asp_Types.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/TTCN3.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/version.h
MTP3asp_Types.o: /usr/include/string.h /usr/include/iso/string_iso.h
MTP3asp_Types.o: /usr/include/sys/feature_tests.h /usr/include/sys/isa_defs.h
MTP3asp_Types.o: /usr/include/stdio.h /usr/include/iso/stdio_iso.h
MTP3asp_Types.o: /usr/include/sys/va_list.h /usr/include/stdio_tag.h
MTP3asp_Types.o: /usr/include/stdio_impl.h
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Basetype.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Types.h
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Encdec.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Template.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Integer.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Optional.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/BER.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Logger.hh
MTP3asp_Types.o: /usr/include/stdlib.h /usr/include/iso/stdlib_iso.h
MTP3asp_Types.o: /usr/include/stdarg.h /usr/include/iso/stdarg_iso.h
MTP3asp_Types.o: /usr/include/sys/time.h /usr/include/sys/types.h
MTP3asp_Types.o: /usr/include/sys/machtypes.h /usr/include/sys/int_types.h
MTP3asp_Types.o: /usr/include/sys/select.h /usr/include/time.h
MTP3asp_Types.o: /usr/include/iso/time_iso.h
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Textbuf.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Error.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Parameters.h
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Float.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Boolean.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/ASN_Null.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Objid.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Verdicttype.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Component.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Bitstring.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/RAW.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Hexstring.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Octetstring.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/ASN_Any.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Charstring.hh
MTP3asp_Types.o: /usr/include/regex.h
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Universal_charstring.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Struct_of.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Array.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/ASN_CharacterString.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/ASN_External.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/ASN_EmbeddedPDV.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Addfunc.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Timer.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Port.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Module_list.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Snapshot.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Default.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Runtime.hh
MTP3asp_Types.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/TEXT.hh
MTP3asp_PortType.o: MTP3asp_PortType.hh MTP3asp_Types.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/TTCN3.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/version.h
MTP3asp_PortType.o: /usr/include/string.h /usr/include/iso/string_iso.h
MTP3asp_PortType.o: /usr/include/sys/feature_tests.h
MTP3asp_PortType.o: /usr/include/sys/isa_defs.h /usr/include/stdio.h
MTP3asp_PortType.o: /usr/include/iso/stdio_iso.h /usr/include/sys/va_list.h
MTP3asp_PortType.o: /usr/include/stdio_tag.h /usr/include/stdio_impl.h
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Basetype.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Types.h
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Encdec.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Template.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Integer.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Optional.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/BER.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Logger.hh
MTP3asp_PortType.o: /usr/include/stdlib.h /usr/include/iso/stdlib_iso.h
MTP3asp_PortType.o: /usr/include/stdarg.h /usr/include/iso/stdarg_iso.h
MTP3asp_PortType.o: /usr/include/sys/time.h /usr/include/sys/types.h
MTP3asp_PortType.o: /usr/include/sys/machtypes.h /usr/include/sys/int_types.h
MTP3asp_PortType.o: /usr/include/sys/select.h /usr/include/time.h
MTP3asp_PortType.o: /usr/include/iso/time_iso.h
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Textbuf.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Error.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Parameters.h
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Float.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Boolean.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/ASN_Null.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Objid.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Verdicttype.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Component.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Bitstring.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/RAW.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Hexstring.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Octetstring.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/ASN_Any.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Charstring.hh
MTP3asp_PortType.o: /usr/include/regex.h
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Universal_charstring.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Struct_of.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Array.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/ASN_CharacterString.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/ASN_External.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/ASN_EmbeddedPDV.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Addfunc.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Timer.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Port.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Module_list.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Snapshot.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Default.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/Runtime.hh
MTP3asp_PortType.o: /mnt/projects/TTCN/Releases/TTCNv3-1.7.pl2-gcc3.4.6/include/TEXT.hh
MTP3asp_PortType.o: MTP3asp_PT.hh
MTP3asp_PortType.o: /vobs/ttcn/TCC_Releases/Other/SEA_LATEST/include/mphclib.h
