ifeq ($(OS),Windows_NT)
	EXT = .exe
else
	EXT =
endif


default: unittests$(EXT)

unittests$(EXT): unittests.cpp ../../readerwriterqueue.h ../../atomicops.h ../common/simplethread.h ../common/simplethread.cpp minitest.h makefile
	g++ -static -std=c++11 -Wpedantic -Wall -DNDEBUG -O3 unittests.cpp ../common/simplethread.cpp -o unittests$(EXT) -pthread

run: unittests$(EXT)
	./unittests$(EXT)
