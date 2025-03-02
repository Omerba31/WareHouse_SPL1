# Compiler
CXX := g++

# Compiler Flags
CXXFLAGS := -g -Wall -Weffc++ -std=c++11 -Iinclude

# Directories
SRC_DIR := src
BIN_DIR := bin
INCLUDE_DIR := include

# Source and Object Files
SRCS := $(wildcard $(SRC_DIR)/*.cpp)
OBJS := $(patsubst $(SRC_DIR)/%.cpp, $(BIN_DIR)/%.o, $(SRCS))

# Executable Name
TARGET := $(BIN_DIR)/warehouse

# Default Rule
all: $(TARGET)

# Compile Source Files
$(BIN_DIR)/%.o: $(SRC_DIR)/%.cpp | $(BIN_DIR)
	$(CXX) $(CXXFLAGS) -c $< -o $@

# Linking
$(TARGET): $(OBJS)
	$(CXX) -o $@ $^

# Run the executable
run: $(TARGET)
	./$(TARGET)

# Debugging Mode
debug: CXXFLAGS += -DDEBUG
debug: clean all

# Clean compiled files
clean:
	rm -rf $(BIN_DIR)/*

# Ensure bin directory exists
$(BIN_DIR):
	mkdir -p $(BIN_DIR)
