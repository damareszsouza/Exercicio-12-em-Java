# Exercicio-12-em-Java
Variáveis de instância - Livro Cartilha Java

A classe Gnome.
Observa-se o uso das variáveis de instância no exemplo da classe Gnome. As 
variáveis age, magical e heightsão de tipos básicos, a variável name é uma referência 
para uma instância da classe predefinida String, e a variável gnomeBuddy é uma refe-
rência para um objeto da classe que está sendo definida. A declaração da variável de 
instância MAX_HEIGHT está tirando proveito desses dois modificadores para definir 
uma “variável” que tem um valor constante fixo. Na verdade, valores constantes asso-
ciados a uma classe sempre devem ser declarados static e final.


public class Gnome {
 // Variáveis de instância:
 public String name;
 public int age;
 public Gnome gnomeBuddy;
 private boolean magical -
 false;
 protected double height -
 2.6;
 public static final int MAX_HEIGHT -
 3; // altura máxima
 // Construtores:
 Gnome(String nm, int ag, Gnome bud, double hgt) { // totalmente parametrizado
 name -
 nm;
 age -
 ag;
 gnomeBuddy -
 bud;
 height -
 hgt;
 }
 Gnome( ) { // Construtor default
 name -
 "Rumple";
 age -
 204;
 gnomeBuddy -
 null;
 height -
 2.1;
 }
 // Métodos:
 public static void makeKing (Gnome h) {
 h.name -
 "King"  h.getRealName( );
 h.magical -
 true; // Apenas a classe Gnome pode referenciar este campo.
 }
 public void makeMeKing ( ) {
 name -
 "King"  getRealName( );
 magical -
 true;
 }
 public boolean isMagical( ) { return magical; }
 public void setHeight(int newHeight) { height -
 newHeight; }
 public String getName( ) { return "I won’t tell!"; }
 public String getRealName( ) { return name; }
 public void renameGnome(String s) { name -
 s; }
}

