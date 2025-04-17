# **SQL** <a href="https://github.com/MiKL5/bi/"><img src="https://github.com/MiKL5/Business_Intelligence/raw/master/assets/bi.svg" alt="Data science" align="right" height="64px"></a>
SQL signifie Structured Query Language. Ce langage de programmation sert à la manipulation des données et RDBMS.  
Ce langage de requête structuré comprend 5 types de commandes.
1. Le **DDL** : **Data Definition Language**.  
   _Définir et modifier la structure_ avec les commandes ’`CREATE`’, ’`ALTER`’, ’`DROP`’ & ’`TRUNCATE`’.
2. Le **DML** : **Data Manipulation Language**.  
   _Gérer le contenu des tables_. Les commandes sont ’`INSERT`’, ’`UPDATE`’, ’`DELETE`’, ’`CALL`’, ’`CALL EXPLAIN`’ & ’`LOCK`’.
3. Le **TCL** : **Transaction Control Language**.  
   _Contrôler (gérer) les transactions par groupe d’opérations_. Ces commandes sont ’`COMMIT`’, ’`SAVEPOINT`’, ’`ROLLBACK`’, ’`SET Transaction`’ & ’`SET Constraint`’.
4. Le **DQL** : **Data Query Language**.  
   _Lire_ par ’`SELECT’.
5. Le **DCL** : **Data Control Language**.  
   _Gérer l’accés_ via les commandes ’`GRANT`’ & ’`REVOKE`’.

<br><div align="center"><br>

```mermaid
flowchart LR
    classDef sql         fill:#000c62,stroke:#000c62,stroke-width:25px;
    classDef ddl         fill:#fea000,stroke:#660,   stroke-width:10px;
    classDef create      fill:#b77f14,stroke:#10,    stroke-width: 0px;
    classDef alter       fill:#b77f14,stroke:#10,    stroke-width: 0px;
    classDef drop        fill:#b77f14,stroke:#10,    stroke-width: 0px;
    classDef truncate    fill:#b77f14,stroke:#10,    stroke-width: 0px;
    classDef dml         fill:#c74375,stroke:#892d95,stroke-width:10px;
    classDef insert      fill:#592147,stroke:#10,    stroke-width: 0px;
    classDef update      fill:#592147,stroke:#10,    stroke-width: 0px;
    classDef delete      fill:#592147,stroke:#10,    stroke-width: 0px;
    classDef 'call'      fill:#592147,stroke:#10,    stroke-width: 0px;
    classDef explain     fill:#592147,stroke:#10,    stroke-width: 0px;
    classDef lock        fill:#592147,stroke:#10,    stroke-width: 0px;
    classDef tcl         fill:#ff4e20,stroke:#e62f00,stroke-width:10px;
    classDef commit      fill:#e62f00,stroke:#10,    stroke-width: 0px;
    classDef savepoint   fill:#e62f00,stroke:#10,    stroke-width: 0px;
    classDef rollback    fill:#e62f00,stroke:#10,    stroke-width: 0px;
    classDef transaction fill:#e62f00,stroke:#10,    stroke-width: 0px;
    classDef constraint  fill:#e62f00,stroke:#10,    stroke-width: 0px;
    classDef dql         fill:#222   ,stroke:#333,   stroke-width:10px;
    classDef select      fill:#111   ,stroke:#10,    stroke-width: 0px;
    classDef dcl         fill:#6d3def,stroke:#3d2eb2,stroke-width:10px;
    classDef grant       fill:#3d2eb2,stroke:#10,    stroke-width: 0px;
    classDef remove      fill:#3d2eb2,stroke:#10,    stroke-width: 0px;

    A((SQL)) --> B[/DDL/]
    A        --> C[/DML/]
    A        --> D[/TCL/]
    A        --> E[\DQL\]
    A        --> F[ DCL ]


    B --> B1(CREATE)
    B --> B2(ALTER)
    B --> B3(DROP)
    B --> B4(TRUNCATE)

    C --> C1(INSERT)
    C --> C2(UPDATE)
    C --> C3(DELETE)
    C --> C4(CALL)
    C --> C5(CALL EXPLAIN)
    C --> C6(LOCK)

    D --> D1(COMMIT)
    D --> D2(SAVEPOINT)
    D --> D3(ROLLBACK)
    D --> D4(SET Transaction)
    D --> D5(SET Constraint)

    E --> E1(SELECT)

    F --> F1(GRANT)
    F --> F2(REMOVE)

    class A sql
    class B ddl
    class C dml
    class D tcl
    class E dql
    class F dcl
    class B1 create
    class B2 alter
    class B3 drop
    class B4 truncate
    class C1 insert
    class C2 update
    class C3 delete
    class C4 'call'
    class C5 explain
    class C6 lock
    class D1 commit
    class D2 savepoint
    class D3 rollback
    class D4 transaction
    class D5 constraint
    class E1 select
    class F1 grant
    class F2 remove
```
<hr>

>Sujets connexes  
[Transact SQL et SQL Server](https://github.com/MiKL5/TSQL/)  
[PostreSQL](https://github.com/MiKL5/PostgreSQL/)  
[SQL vs Transact SQL vs Procedural SQL](https://github.com/MiKL5/TSQL/docs/comprae)