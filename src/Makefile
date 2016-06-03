CXX=g++
CPPFLAGS += -I../include
LDFLAGS += -L../lib -lmemcached -lpthread

SRC_DIR := src
BUILD_DIR := ../build
BIN_DIR := ../bin
OBJECT := test.o

all : dbcache

dbcache : ${OBJECT} 
	$(CXX) $^ $(LDFLAGS) -o $(BIN_DIR)/$@

$(BUILD_DIR)/%.o : %.cpp
	$(CXX) $< $(CPPFLAGS) -c -o $@ 

clean:
	@rm -rf $(OBJECT) $(BIN_DIR)/$@

