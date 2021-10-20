# Compiler Design Project
## About The Project
This is the final project of the Principles of Compiler Design course using Lex & Yacc.
### Contributers
[Mahan Ahmadvand](https://github.com/2000mahan) <br />
[Mohammad Sami](https://github.com/MohammadMDSA) <br />

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
`program -> declist main () block` <br />
`declist -> dec | declist dec | ε` <br />
`dec -> vardec | funcdec` <br />
`type -> int | float | bool` <br />
`iddec -> id |id [exp] | id=exp` <br />
`idlist -> iddec | idlist, iddec` <br />
`vardec -> idlist:type;` <br />
`funcdec -> fun id (paramdecs):type block | fun id (paramdecs) block` <br />
`paramdecs -> paramdecslist | ε` <br />
`paramdecslist -> paramdec | paramdecslist, paramdec` <br />
`paramdec -> id:type | id []:type` <br />
`block -> {stmtlist}` <br />
`stmtlist -> stmt | stmlist stmt | ε` <br />
`lvalue -> id | id[exp]` <br />
`case -> where const:stmtlist` <br />
`cases -> case | cases case | ε` <br />
`stmt -> return exp; | exp; | block | vardec | while (exp) stmt | on (exp) {cases}; | for (exp; exp; exp) stmt | for (id in id) stmt | if (exp) stmt elseiflist | if (exp) stmt elseif else stmt | print (id)` <br />
`elseiflist -> elseif (exp) stmt | elseiflist elseif (exp) stmt | ε` <br />
`relopexp -> exp relop exp | relopexp relop exp` <br />
`exp -> lvalue=exp | exp operator exp | relopexp | const | lvalue | id (explist) | (exp) | id () | - exp | not exp` <br />
`operator -> and | or | + | - | * | / | %` <br />
`const -> intnumber | floatnumber | True | False` <br />
`relop -> > | < | != | == | <= | >=` <br />
`explist -> exp | explist, exp` <br />

## Phase 3(Intermediate Code Generation)
![alt text](https://s4.uupload.ir/files/phase3_4te.png)
