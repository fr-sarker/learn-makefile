# Compiler settings
CC = gcc
CXX = g++

# Compiler flags
CFLAGS = -Wall -Wextra -g
CXXFLAGS = -Wall -Wextra -g

# Find all C and C++ source files
C_SRCS := $(wildcard *.c)
CPP_SRCS := $(wildcard *.cpp)

# Convert source files to executables
C_BINS := $(C_SRCS:.c=)
CPP_BINS := $(CPP_SRCS:.cpp=)
BINS := $(C_BINS) $(CPP_BINS)

# Default target: compile all
all: $(BINS)

# Compile C files into executables
%: %.c
	@echo "Compiling C program: $@"
	$(CC) $(CFLAGS) $< -o $@

# Compile C++ files into executables
%: %.cpp
	@echo "Compiling C++ program: $@"
	$(CXX) $(CXXFLAGS) $< -o $@

# Run a specific program
run: 
	@echo "Usage: make run PROGRAM=<executable>"
	@./$(PROGRAM)

# Clean all compiled files
clean:
	@echo "Cleaning up..."
	rm -rf $(BINS)
