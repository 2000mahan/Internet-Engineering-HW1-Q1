# Compiler Design Project
## About The Project
This is the final project of the Principles of Compiler Design course using Lex & Yacc.
## Phase 1(Lexical Analyzer)
| Lexeme        | Token Value   |
| ------------- |:-------------:|
| Identifier    | ID |
| Integer number| INTEGERNUMBER |
| Float number  | FLOATNUMBER   |
| "int"         | INTEGER       |
| "float"       | FLOAT         |
| "bool"        | BOOLEAN       |
| "fun"         | FUNCTION      |
| "True"        | TRUE          |
| "False"       | FALSE         |
| "print"       | PRINT         |
| "return"      | RETURN        |
| "main"        | MAIN          |
| "if"          | IF            |
| "else"        | ELSE          |
| "elseif"      | ELSEIF        |
| "while"       | WHILE         |
| "on"          | ON            |
| "where"       | WHERE         |
| "for"         | FOR           |
| "and"         | AND           |
| "or"          | OR            |
| "not"         | NOT           |
| "in"          | IN            |
| "="           | ASSIGN        |
| "+"           | SUM           |
| "-"           | SUB           |  
| "*"           | MUL           |
| "/"           | DIV           |
| "%"           | MOD           |
| ">"           | GT            | 
| ">="          | GE            |
| "<"           | LT            |
| "<="          | LE            |
| "=="          | EQ            |
| "!="          | NE            |
| "{"           | LCB           |
| "}"           | RCB           |
| "("           | LRB           |
| ")"           | RRB           |
| "\["          | LSB           |
| "\]"          | RSB           |
| ";"           | SEMICOLON     |
| ":"           | COLON         |
| ","           | COMMA         |
| "Error"       | ERROR!        |

## Phase 2(Parser)
### Grammar :
`program -> declist main () block`

throughout the course according to what you have learnt we expect you to make some modifications so that you will get to know the  xv6 operating system better and you will see that developing an operating system is not as hard as you imagined and it is just a piece of cake.
## How are you going to make theses modifications?
Well your xv6 project is divided into three phases.
In the first two phases we want you to make some modifications to get to know with xv6 operating system and during that we will be available to help you throughout the course so don’t worry.
In the third phase what you are going to do, is to make some modifications to xv6 just like what you have done in the first two phases but it is going to be a little bit of challenge.
## How are you going to do it?
The very first thing we want you to do is to create teams of two members(this is for third phase) and create a private GitHub repository so that we can see you making progress(you could either add me or the instructor to your git repository).
You could also use gitlab or other repository managers but we prefer GitHub.
## xv6 Sources :
#### The latest xv6 source is available via : 
git clone git://pdos.csail.mit.edu/xv6/xv6.git
## Xv6 kernel hacking 
### These three phases all are to be done inside the xv6 kernel based on an early version of Unix and developed at MIT. 
#### Phase 1 (intro) 
This first phase is just a warmup and is for you to engage with xv6.
In the first phase and in your very first experience with xv6 you are expected to add two system calls to xv6.
First you need to setup a virtual machine(recommended) and install a fresh ubuntu operating system on it and then you need to install qemu virtual machine so that you will be able to run xv6 on qemu.

- `int getreadcount(void)`    
Returns the value of a counter which is incremented every time any process calls the read() system call.   
You have to define a variable for the values of read counter. (e.g. readcount)  

- `int getprocs(void)`    
returns the number of processes that exist in the system at the time of the call.

Taken from the University of Wisconsin-Madison operating systems course projects.

#### Phase 2
In this part you are going to make some crucial modifications. <br />
#### Phase 3 (main)
In this part you are going to make some crucial modifications. <br />
#### Staff
Instructor: [Dr.Seyyed Ahmad Javadi](https://github.com/sajavadi) <br />
Course Assistant: [Mahan Ahmadvand](https://github.com/2000mahan) <br />
Course Assistant: [Arman Hatami](https://github.com/armanhtm) <br />
Course Assistant: [Mahdi Rezaie](https://github.com/mahdirezaie336) <br />
Course Assistant: [Mahdi Rahmani](https://github.com/Mahdi-Rahmani) <br />
Course Assistant: [Mohammad Reza Qaderi](https://github.com/MohammadRezaQaderi) <br />
