filename=  Makefile_v       #name of the folder having makefile

all: myapp

CC=gcc

INCLUDES=.

LIBS = -lc

OBJS= myadd.o prog1.o mysub.o mydiv.o mymul.o ./d1/mymod.o

INSTDIR = /usr/bin


myapp: $(OBJS)

	$(CC) -o myapp $(OBJS)  $(LIBS)

myadd.o: myadd.c
 
	$(CC) -c myadd.c

mysub.o: mysub.c

	$(CC) -c mysub.c
 
mydiv.o: mydiv.c

	$(CC) -c mydiv.c
  
mymul.o: mymul.c

	$(CC) -c mymul.c
  
prog1.o: prog1.c mymath.h ./d1/mymod.h

	$(CC) -c prog1.c -I$(INCLUDES)


include: ./d1/makefile


clean:
	-@rm -f $(OBJS)


install: 
myexe
	@if [ -d $(INSTDIR) ]; 
\
	then \

		cp myexe $(INSTDIR) && \

		chmod a+x $(INSTDIR)/myapp && \
	
	chmod og-w $(INSTDIR)/myapp && \
		
echo "myexe installed successfully in $(INSTDIR)"; \
	
fi


uninstall:
	
@rm -f $(INSTDIR)/myapp

	@echo "myexe successfully un-installed from $(INSTDIR)"

