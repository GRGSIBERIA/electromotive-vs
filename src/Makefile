CC = g++
CFLAGS =
TARGET = electromotive
SRCS = main.cpp
# for example
# SRCS += compute.cpp
# SRCS += tetrahedon.cpp
OBJS = $(SRCS:.cpp=.o)
INCDIR = -I../inc
LIBDIR = -L/usr/local/lib -L/lib/x86_64-linux-gnu/
LIBS = -liostream

$(TARGET): $(OBJS)
	$(CC) -o $@ $^ $(LIBDIR) $(LIBS)

$(OBJS): $(SRCS)
	$(CC) $(CFLAGS) $(INCDIR) -c $(SRCS)

all: clean $(OBJS) $(TARGET)
clean:
	-rm -f $(OBJS) $(TARGET) *.d