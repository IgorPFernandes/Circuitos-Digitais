# Circuitos-Digitais

<br>

##Exercício 1:
=

%%file exercicio.sv


Módulo exercicio

module exercicio(a,b,c,z);

  // Declaração de portas
  input a,b,c;
  ouput z;
  // Variáveis (fios) intermediárias
  wire nc,nb,na,p0,p1,p2;

  // Estrutura
  not not0 (nc,c);
  <br>
  not not1 (nb,b);
  <br>
  not not2 (na,a);
  <br>
  and and0 (p0,c,nb);
  <br>
  or or0 (p1,nc,a);
  <br>
  and and1 (p2,na,b);
  <br>
  or orf (z,p0,p1,p2);


endmodule


<br>



##Exercício 2:
=

module exercicio2(i0,i1,a,q);

input i0,i1,a;
output q;

wire p1,p2,p3;

nand nand0 (p1,a,a);
<br>
nand nand1 (p2,i0,a);
<br>
nand nand2 (p3,i1,p1);
<br>
nand nand3 (q,p2,p3);

endmodule



<br>


##Exercício 3:
=

module exercicio3(a,b,c,d,e);

input a,b;
output c,d,e;

wire n1,n2,p1,p2;

not not1 (n1,a);
<br>
not not2 (n2,b);
<br>
and and1 (p1,b,n1);
<br>
and and2 (p2,a,n2);
<br>
and andc (c,a,n2);
<br>
and and3 (e,b,n1);
<br>
or or1 (d,p1,p2);

endmodule
