Taller 1

Exercicis 1 i 2 crea la llista l'usuari
Exercici 3 la llista ya està creada

ALGORISMES DE CREACIONS DE LLISTES

1) CREACIÓ LLISTA LINEAL NODES INSEREIXEN A L'INICI

Var Capçalera, Nounode : ^ element_llista;

BEGIN
    Read/Llegir/Leer(n); //(sent "n" els nodes que contidrà la llista)
    Capçalera := nil;
    WHILE n>0 DO
       BEGIN     
        new(Nounode);
        Nounode^.seg := Capçalera;
        Capçalera := Nounode;
        (Nounode^.info := {dades}) //això dona igual on posar-ho? 
                                   // sent dades informació que introdueix l'usuari
        n := n-1;
        END //no sé si fa falta 
END                                   

    
2) CREACIÓ LLISTA LINEAL NODE INSEREIXENÇ AL FINAL

Var Capçalera, Nounode, Darrer : ^ element_llista;

BEGIN
    //inserir el primer node a la llista
    Read/Llegir/Leer(n); //(sent "n" els nodes que contidrà la llista)
    Capçalera := nil;
    Darrer_node := nil;
    IF n>0 THEN
        BEGIN
        new(Nounode);
        Capçalera := Nounode;
        Darrer:= Nounode;
        Darrer^.info := {dades};
        n := n-1; //fins aquí tenim primer node 
        
        //ara incorporam la resta a la llista 
        WHILE n>0 DO
          BEGIN     
            new(Nounode);
            Darrer^.seg := Nounode;
            Darrer := Nounode;
             Darrer^.info := {dades};
            n := n-1; 
          END
          Darrer^.seg := Nounode; //això no importa perquè ja apunta a nil
     END //(ELSE Imprimir("Lista vacía quiere una aletoria? s/n"))    
END

INSERCIÓ D'UN NODE DAVANT UN DE DONAT

- Llista apuntada per variable capçalera
- El contigut del node a cercar per inserir el nou_node el ficarà l'usuari
- Imprimir per pantalla la Llista
    

ELIMINACIÓ D'UN ELEMENT DONAT 

INSERCIÓ D'UN ELEMENT EN UNA LLISTA ORDENADA

-Llista ordenada menor a mayor orden creciente (1,2...6)
- Insereix davant el node a cercar que introdueix l'usuari
-Inserció com execercici 1, a l'esquerra

LLISTA DOBLEMENT ENCADENADES

