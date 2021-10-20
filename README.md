# Compiler Design Project
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#contributers">Contributers</a></li>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
    <li>
      <a href="#phases">Phases</a>
      <ul>
        <li><a href="#phase-1(Lexical-Analyzer)">Phase 1(Lexical Analyzer)</a></li>
        <li>
          <a href="#phase-2(Parser)">Phase 2(Parser)</a>
          <li><a href="#grammar">Grammar</a></li>
        </li>
        <li><a href="#phase-3(Intermediate-Code-Generation)">Phase 3(Intermediate Code Generation)</a></li>
    </li>
  </ol>
</details>

## About The Project
This is the final project of the Principles of Compiler Design course using Lex & Yacc.
### Contributers
[Mahan Ahmadvand](https://github.com/2000mahan) <br />
[Mohammad Sami](https://github.com/MohammadMDSA) <br />

### Built With

* [PLY (Python Lex-Yacc)](https://www.dabeaz.com/ply/)
* [Python](https://www.python.org)

## License

Distributed under the GNU License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#top">back to top</a>)</p>

## Contact

Your Name - Mahan Ahmadvand

Project Link: [https://github.com/2000mahan/web-engineering-HW1](https://github.com/2000mahan/web-engineering-HW1)

<p align="right">(<a href="#top">back to top</a>)</p>

## Acknowledgments

* [https://www.python.org/doc/](https://www.python.org/doc/)
* [https://www.dabeaz.com/ply/](https://www.dabeaz.com/ply/)

<p align="right">(<a href="#top">back to top</a>)</p>

## Phases

### Phase 1(Lexical Analyzer)
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

<p align="right">(<a href="#top">back to top</a>)</p>

### Phase 2(Parser)
#### Grammar :
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

<p align="right">(<a href="#top">back to top</a>)</p>

### Phase 3(Intermediate Code Generation)
![alt text](https://s4.uupload.ir/files/phase3_4te.png)

<p align="right">(<a href="#top">back to top</a>)</p>
