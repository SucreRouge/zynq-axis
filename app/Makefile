CC = ${CROSS_COMPILE}gcc
LDFLAGS := -linterface
CFLAGS := -c -Wall -Werror
INCLUDES := -I.

EXECUTABLE = \
	write-memory \
	read-memory \
	test-mem \
	test-cfg


.PHONY : all
all : $(EXECUTABLE)


.c.o :
	$(CC) $(INCLUDES) $(CFLAGS) $< -o $@


write-memory : write-memory.o
	$(CC) $< -o $@ $(LDFLAGS)


read-memory : read-memory.o
	$(CC) $< -o $@ $(LDFLAGS)


test-mem : test-mem.o
	$(CC) $< -o $@ $(LDFLAGS)


test-cfg : test-cfg.o
	$(CC) $< -o $@ $(LDFLAGS)


.PHONY : clean
clean :
	rm -f *.o $(EXECUTABLE)
