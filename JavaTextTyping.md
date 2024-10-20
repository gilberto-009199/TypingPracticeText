## Java Texts

### Java Words Reservate Complete
```java
java package import abstract class interface enum record implements extends public private protected synchronized strictfp transient volatile native static void final for do while continue if else switch case break default try catch finally return boolean byte char int short long float double String new this super instanceof throw throws assert
```

### Java Example API Stream
```java
int[] numeros = {1, 2, 3};
IntStream stream = Arrays.stream(numeros).filter(n -> n % 2 == 0);
stream.forEach(System.out::println);
int soma = Arrays.stream(numeros).sum();
String[] frutas = {"Maçã", "Banana", "Laranja"};
Arrays.stream(frutas).map(String::toUpperCase).forEach(System.out::println);
long count = Arrays.stream(frutas).filter(f -> f.length() > 5).count();
```
### Java Example List Simple 
```java
List<String> lista = new ArrayList<>();
lista.add("two");
lista.add("tree");
lista.add("five");
for(String fruta : lista){
out.println(fruta);
}
for(int i = 0; i < lista.size(); i++){
out.println(lista.get(i));
}
```
### Java Example In And Output
```java
Scanner scanner = new Scanner(System.in);
String in = scanner.nextLine();
if(in.equals("gil")){
out.println("equals == 'gil'.");
}else{
out.println("not equals != 'gil'");
}
scanner.close();
```
### Java Example Set
```java
Set<String> conjunto = new HashSet<>();
conjunto.add("one");
conjunto.add("two");
conjunto.add("tree");
if(conjunto.contains("tree")){
out.println("tree in set.");
}else{
out.println("tree not in set");
}
conjunto.remove("tree");
for(String fruta : conjunto){
out.println(fruta);
}
```

### Java Example Stack
```java
Stack<String> pilha = new Stack<>();
pilha.push("one");
pilha.push("two");
pilha.push("tree");
out.println("top in stack:"+ pilha.peek());
out.println("remove top in stack:"+ pilha.pop());
if(pilha.isEmpty()){
out.println("stack empty");
}else{
out.println("stack not empty");
}
int posicao = pilha.search("tree");
if(posicao != -1){
out.println("the 'tree' in position: " + posicao);
}else{
out.println("the 'tree' not in stack");
}
```