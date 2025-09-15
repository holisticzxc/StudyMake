.PHONY: all debug release clean

# Переменные
SRC_FILE = Kazino-Royal.cpp
RELEASE_FLAGS = -O2 -Wall -DNDEBUG
DEBUG_FLAGS   = -g -O0 -Wall
RELEASE_EXEC = kazino
DEBUG_EXEC   = kazino-dbg

# Правила
all: debug release

debug: $(DEBUG_EXEC)

$(DEBUG_EXEC): $(SRC_FILE)
	g++ $(DEBUG_FLAGS) $(SRC_FILE) -o $(DEBUG_EXEC)

release: $(RELEASE_EXEC)

$(RELEASE_EXEC): $(SRC_FILE)
	g++ $(RELEASE_FLAGS) $(SRC_FILE) -o $(RELEASE_EXEC)

clean:
	rm -f $(RELEASE_EXEC) $(DEBUG_EXEC)
