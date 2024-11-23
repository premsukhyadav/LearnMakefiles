#####################################
#	variables
#####################################

TARGET := final_executable

CC := gcc
CFLAGS := -Wall -Wextra

#####################################
#	Targets
#####################################

$(TARGET): main.o
	$(CC) $(CFLAGS) -o $(TARGET) main.o
	
main.o: main.c
	$(CC) $(CFLAGS) -c main.c -o main.o
	
clean:
	rm -f $(TARGET) main.o # use "del" on Windows