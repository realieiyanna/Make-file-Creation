# Name: Iyanna Woods
# File: Makefile
# Date: Februrary 21st, 2026
# Description/purpose: To create a makefile for an employee project


#Variables

# CC is being used for the compiler which is g++
CC = g++

#C flags are used for things like -c, -Wall, -Wextra
CFLAGS = -c -Wall -Wextra

#TARGET (Goal) is the execuatnle for the names of the employees
#Name of final program that you want to run
TARGET = employee

#The actual makefile that places everythin together like $() are like variables that hodl bvalue when called, these can link files, compile erros
all: $(TARGET)

$(TARGET): main.o Employee.o Officer.o Supervisor.o
	$(CC) main.o Employee.o Officer.o Supervisor.o -o $(TARGET)


#Placing all of the header files together in main "collecting"
main.o: main.cpp Employee.h Officer.h Supervisor.h
	$(CC) $(CFLAGS) main.cpp

# Compiling all of the files
Employee.o: Employee.cpp Employee.h
	$(CC) $(CFLAGS) Employee.cpp

Officer.o: Officer.cpp Officer.h
	$(CC) $(CFLAGS) Officer.cpp

Supervisor.o: Supervisor.cpp Supervisor.h
	$(CC) $(CFLAGS) Supervisor.cpp

#This removes already compiled files and works as a "Clean up function"
clean:
	rm -f *.o $(TARGET)
