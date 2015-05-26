# LINK

#Reasearch on static lib linking.
#
#unix> gcc -c addvec.c multvec.c
#unix> ar rcs libverctor.a addvec.c multvec.c
#unix> gcc -O2 -c main2.c
#unix> gcc -static -o p2 main2.o ./libvector.a
#
#-static参数告诉编译驱动程序，需要构造一个完全链接的可执行目标文件，可以加载到存储器运行。当连接器运行时，它判断addvec.o定义的符号addvec是被main.o使用的，所以它会拷贝addvec.o到可执行文件；multvec.o定义的multvec没有使用，因此不会被拷贝进去。
#
