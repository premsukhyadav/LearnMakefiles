# Variables in Makefile
Variables store reusable values to simplify and organize the Makefile

These are the 3 variables that we are using in this file
* TARGET := final_executable
* CC := gcc
* CFLAGS := -Wall -Wextra

This makes it easy to reuse and change the variables in one place
without modifying multiple lines in the Makefile. If you want to switch 
to a different compiler (e.g., clang), you can do it just by modifying  variable _$(CC)_. We can customize these flags (e.g., add optimization flags like -O2)
as needed, and the changes will apply everywhere automatically.

# Build the project

    # If we just write make by default it looks for first target
	>terminal:
	make
	
The make command looks at the Makefile and runs the first target (final_executable).
It checks if main.o exists as target depends on main.o

Now it sees that main.c is needed to get main.o, hence it compiles main.c into main.o and links it to create the executable final_executable.

    # This is what you see in terminal after running make
    >terminal:
    gcc -Wall -Wextra -c main.c -o main.o
    gcc -Wall -Wextra -o final_executable main.o

You can see that the main.o is generated first followed by generateing executable.

# Clean the project

    # This time we will specify the target that we want to run from makefile
    >terminal:
    make clean

The clean target deletes final_executable and main.o, resetting the directory.
This is useful for starting fresh or clearing old build files.

    # This is what you see in terminal after running main.
    > terminal:
    rm -f final_executable main.o # use "del" on Windows

This ensure that target clean got executed