# Усложненный make-file.  Введены переменные для параметров компиляции и исполняемых файлов

.PHONY: all debug release clean

SRC_FILE = hello.cpp
RELEASE_FLAGS = -O2 -Wall -DNDEBUG
DEBUG_FLAGS   = -g -O0 -Wall
RELEASE_EXEC = hello
DEBUG_EXEC   = hello-dbg

all: debug release

debug: $(DEBUG_EXEC)

$(DEBUG_EXEC): $(SRC_FILE)
	g++ $(DEBUG_FLAGS) $(SRC_FILE) -o $(DEBUG_EXEC)

release: $(RELEASE_EXEC)

$(RELEASE_EXEC): $(SRC_FILE)
	g++ $(RELEASE_FLAGS) $(SRC_FILE) -o $(RELEASE_EXEC)

clean:
	rm -f $(RELEASE_EXEC) $(DEBUG_EXEC)

