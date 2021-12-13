obj = main.o world.o znak.o

.PHONY: hello clean cloon install uninstall district wc help test
.DEFAULT:
	@echo 'Ошибка'
	@make help

hello: $(obj)
	gcc -o hello $(obj)
 
main.o: main.c
	gcc -c main.c

world.o: world.c
	gcc -c world.c

znak.o: znak.c
	gcc -c znak.c

install:
	install ./hello /home/02/tverdohl/bin

uninstall:
	rm -rf /home/02/tverdohl/bin/hello

district:
	tar -cvf hello.tar main.c world.c znak.c Makefile

doc:
	doxygen config        

help:
	@chmod ugo+x bash_info
	@./bash_info

clean:
	rm hello *.o

cloon:
	rm *.o

wc:
	@echo "Количество строк: "
	@wc -l main.c
	@wc -l world.c
	@wc -l znak.c

test: hello
	@./hello

