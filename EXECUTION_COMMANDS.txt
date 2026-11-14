### Prerequisites

Install the required compiler tools in Ubuntu/Linux:

```bash
sudo apt update
sudo apt install flex bison gcc build-essential
```

Clone the repository:

```bash
git clone https://github.com/Honeykalastar/Compiler_Construction_Lab.git
cd Compiler_Construction_Lab
```

---

### Practical 1 – Lexical Analysis

**Program 1:**

```bash
cd Practical-1
flex My_First_Progm.l
gcc lex.yy.c -o p1a -lfl
./p1a
```

**Program 2:**

```bash
flex My_Second_Progm.l
gcc lex.yy.c -o p1b -lfl
./p1b
```

### Practical 2 – Count Comments, Keywords and Identifiers

```bash
cd Practical-2
flex 'Count(num of comments,keywords,identifiers).l'
gcc lex.yy.c -o p2 -lfl
./p2
```

### Practical 3 – Count Words Starting with 'A'

```bash
cd Practical-3
flex "Count(num of words starting with 'A').l"
gcc lex.yy.c -o p3 -lfl
./p3
```

### Practical 4 – Introduction to YACC Tool

**Introduction to YACC Lex program:**

```bash
cd Practical-4
flex Intro_to_yacc_tool.l
gcc lex.yy.c -o intro -lfl
./intro
```

**Lex and YACC Parser:**

```bash
yacc -d Parser.y
flex lex2.l
gcc y.tab.c lex.yy.c -o parser -lfl
./parser
```

### Practical 5 – Conversion of Lowercase to Uppercase

```bash
cd Practical-5
flex Coversion_of_lower_to_uppercase.l
gcc lex.yy.c -o p5 -lfl
./p5
```

### Practical 6

Refer to the `Practical-6.1` and `Practical-6.2` subfolders for their respective source files and execution instructions.

### Practical 7 – Check Whether a String Ends with .com

```bash
cd Practical-7
flex Ends_with_com.l
gcc lex.yy.c -o p7 -lfl
./p7
```

### Practical 8 – Postfix Expression

```bash
cd Practical-8
yacc -d postfix.y
flex postfix.l
gcc y.tab.c lex.yy.c -o p8 -lfl
./p8
```

### Practical 9

```bash
cd Practical-9
yacc -d p9.y
flex p9.l
gcc y.tab.c lex.yy.c -o p9 -lfl
./p9
```

### Practical 10

```bash
cd Practical-10
yacc -d p10.y
flex p10.l
gcc y.tab.c lex.yy.c -o p10 -lfl
./p10
```

---

### Notes

- Run the commands from the respective practical directory.
- Run `flex` before compiling Lex programs.
- For YACC programs, run `yacc -d` before `flex` and GCC.
- `lex.yy.c`, `y.tab.c` and `y.tab.h` are generated automatically.
- Use `Ctrl + C` to stop a program if it is waiting for input.
- Use `Ctrl + D` to send EOF when required.
