# Pointers

In C/C++ programming, a pointer is a **variable that stores the memory address of another variable**. Pointers are used to store the addresses of other variables or **memory locations**, and they can be used to indirectly access the stored data.

    1. A pointer variable stores the **memory address** of another variable.
    2. Pointers are declared by placing an asterisk "**`*`**" in front of the variable name.
    3. The "**`&`**" operator is used to obtain the memory address of a variable.
    4. The "**`*`**" operator is used to indirectly access the value stored at a memory address.
    5. Pointers can be used to efficiently pass large amounts of data to functions and to manipulate dynamic data structures such as linked lists and trees.

## How to work with pointers:

```c
int a; // integer
int* pointer_of_a; // pointer to integer

char c; // character
char* pointer_of_c; // pointer to character

double d; // real number
double* pointer_of_d; // pointer to real number

pointer_of_a = &a; // &a is equal to memory adress of a
...
pointer_of_d = &d; // &d is equal to memory adress of d

// prints the memory adress where pointer_of_a points
printf("%d\n", pointer_of_a);

// prints the value, stored in the memory where pointer_of_a points
printf("%d\n", *pointer_of_a); // dereferencing

// prints the memory adress of a
printf("%d\n", &a); // &a = adress of a
```

## Pointer arithmetic

The **size** of **data types** in computer memory can vary depending on the specific data type and the computer's architecture. In general, though, most data types have a **fixed size** that is determined by the programming language and the computer's hardware. For example, a **float data type** (*used to represent floating-point numbers / real numbers*) typically takes up **4 bytes** of memory on a **32-bit system**, while a **double data type** (*used to represent double-precision floating-point numbers / real numbers*) typically takes up **8 bytes** of memory on a 64-bit system.

You can get the size of a data type or variable by using the built-in function `sizeof()`.

```c
int size_of_int = sizeof(int); // 4 bytes
int size_of_char = sizeof(char); // 1 byte
int size_of_float = sizeof(float); // 4 bytes 
int size_of_double = sizeof(double); // 8 bytes
```

```c
int a = 10;
int* p = &a;

// pointer arithmetic
printf("Adresss of a is %d\n", p); // p is 2002
printf("Size of integer is %d bytes\n", sizeof(int));
printf("Adress p+1 is %d\n", p + 1); // p+1 is 2006
```

## Understanding bytes in memory

    In a computer's memory, a **byte** is a unit of data that is typically composed of **8 bits**. Bytes are often used to represent a character such as a **letter**, **number**, or symbol in a computer's memory.

    **Binary** is the language that is used to encode data. A binary digit, or **bit**, is the basic unit of information in computing and digital communications. A bit has a single binary **value of either 0 or 1**.

![asdf](/pics/2.png)

```c
int a = 1025;
int* p = &a;

printf("Size of integer is %d bytes\n", sizeof(int));
printf("Address of a = %d, value of a = %d\n", p, *p);

char *p0;
p0 = (char*)p; // typecasting

printf("Size of char is %d bytes\n", sizeof(char));
printf("Address of a = %d, value of a = %d\n", p0, *p0);

/*

1025 = 00000000 00000000 00000100 00000001 - 4 bytes, 32 bits

value of *p0 = 1, because character type stores 1 byte of memory
the first and only byte of pointer p0 is 00000001, which represents the value 1 in binary

*/
```



