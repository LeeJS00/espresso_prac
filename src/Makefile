SRC := $(wildcard ./espresso-src/*.c)

OBJ := ${SRC:.c=.o}

OBJ_DIR := ./obj

TARGETDIR := ../bin

#TARGET := $(TARGETDIR)/espresso
TARGET := espresso

OBJECTS := $(patsubst %.o,$(OBJ_DIR)/$.o,$(OBJ))

CXXFLAGS = -std=c++17 -W -Wall -O3 -m64 

all: prepare $(TARGET)

prepare:
	mkdir -p $(TARGETDIR)

$(TARGET): $(OBJ) $
	g++ $(CXXFLAGS) -c main.cpp
	gcc -c $(SRC)
	g++ -o $(TARGET) main.o $(OBJ)

.PHONY: clean all

clean: 
	@- $(RM) $(TARGET)
	@- $(RM) $(OBJ)
	rm -f *.o

