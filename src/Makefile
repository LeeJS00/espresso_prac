SRC := $(wildcard ./espresso-src/*.c)

OBJ := ${SRC:.c=.o}

TARGETDIR := ../bin

TARGET := $(TARGETDIR)/espresso

#CXXFLAGS = -std=c++17 -W -Wall -O3 -m64 

all: prepare $(TARGET)

prepare:
	mkdir -p $(TARGETDIR)

$(TARGET): $(OBJ) $
	g++ -c main.cpp
	gcc -c $(OBJ)
	g++ -o $(TARGET) main.o $(OBJ)

.PHONY: clean all

clean: 
	@- $(RM) $(TARGET)
	@- $(RM) $(OBJ)

