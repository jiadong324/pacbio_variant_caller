PWD=$(shell pwd)

all: lib/libhdf5_cpp.so

lib/libhdf5_cpp.so: hdf5-1.8.15-patch1
	cd $< && ./configure --enable-cxx --prefix=$(PWD) && make install clean

hdf5-1.8.15-patch1 : hdf5-1.8.15-patch1.tar.gz
	tar zxvf $<

hdf5-1.8.15-patch1.tar.gz :
	wget https://support.hdfgroup.org/ftp/HDF5/releases/hdf5-1.8/hdf5-1.8.15-patch1/src/$@ -O $@

.PHONY : clean

clean :
	rm -rf hdf5-1.8.15*; rm -rf bin include lib share;