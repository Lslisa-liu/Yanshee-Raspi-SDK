#Makefile
CFLAGS = -Wall -ggdb -g3 -fPIC

SOURCES = cJSON.c

OBJS = $(SOURCES:.c=.o)
DEPENDS = .depend

INCLUDE_PATH = -I. -I../../include
CFLAGS +=  $(INCLUDE_PATH) 

ARFLAGS = -rv

SHLIB = libjson.so
LIBS = $(SHLIB)

LDFLAGS += -shared -fPIC

all: $(SHLIB)
	
$(SHLIB):$(OBJS)
	$(CC)  $(LDFLAGS) -Wall -g -O0 -o $@ $(OBJS) -lm

clean:
	rm -f $(OBJS) $(LIBS) $(DEPENDS)

	
