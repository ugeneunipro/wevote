#CXX = g++
#CXX = /opt/homebrew/bin/g++-11
#CXX = /opt/homebrew/bin/x86_64-elf-g++
CXX=/usr/local/bin/g++-11
CXXFLAGS = -Wall -fopenmp -O3 -m64 -L./ -lstdc++ -lgomp -lgcc_s.1 -v -mmacosx-version-min=10.13.6

LDFLAGS="-L./"
LIBRARY_PATH=./

PROGS = WEVOTE ABUNDANCE

.PHONY: all install clean

all: $(PROGS)

install: $(PROGS)

install: $(PROGS)
	cp $(PROGS) ../bin/

clean:
	rm -f $(PROGS) *.o

WEVOTE: helpers.o create_db.o
ABUNDANCE: helpers.o create_db.o
helpers.o: helpers.cpp helpers.hpp
	$(CXX) $(CXXFLAGS) -c helpers.cpp

create_db.o: create_db.cpp create_db.hpp
	$(CXX) $(CXXFLAGS) -c create_db.cpp
	

