#Name: Luca Matsumoto
#ID: 204726167
#Email: lucamatsumoto@gmail.com

.SILENT:

build:
	gcc -g -Wall -Wextra -pthread lab2_add.c -o lab2_add
	gcc -g -Wall -Wextra -pthread lab2_list.c SortedList.c -o lab2_list

tests: build 
	chmod +x tester.sh
	./tester.sh

graphs: tests
	chmod +x lab2_add.gp
	chmod +x lab2_list.gp
	./lab2_add.gp
	./lab2_list.gp

dist: build graphs
	tar -cvzf lab2a-204726167.tar.gz SortedList.h SortedList.c lab2_list.c lab2_add.c *.png lab2_add.csv tester.sh lab2_list.csv README Makefile lab2_add.gp lab2_list.gp

clean:
	rm -f *.o lab2_add lab2_list *.tar.gz


