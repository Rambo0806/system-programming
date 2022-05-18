cc = g++
BIN = bin/
OBJ = obj/
INC = include/
SRC = src/
CFLAG = -c
OFLAG = -o
all: clean build-server build-client

build-server: ${OBJ}func.o
	${cc} ${OFLAG} ${BIN}server30 ${SRC}server.cpp ${OBJ}func.o
$(OBJ)func.o:
	${cc} ${CFLAG} ${OFLAG} ${OBJ}func.o ${SRC}func.cpp

build-client:
	${cc} ${OFLAG} ${BIN}client30 ${SRC}client.cpp

start-server:
	./${BIN}server30
start-client:
	./${BIN}client30
clean:
	rm ${OBJ}func.o
	rm ${BIN}client30
	rm ${BIN}server30
