# Questão 1

> Explique qual a função da Máquina Virtual Java (JVM).

A **JVM** tem a função de interpretar os códigos em bytecode (.class) os traduzindo para um formato que o sistema operacional compreenda. É ela que permite que um mesmo bytecode seja executado em diferentes sistemas operacionais sem precisar de  alteração, contanto que a **JVM** esteja instalada.

# Questão 2

> Qual a diferença entre JRE e JDK?

De forma simplificada ambos são diferentes por causa que:

* A **JRE** é o ambiente de Execução do Java, ao qual **fornece as bibliotecas** padrões do Java. 
* Já o **JDK** é o kit de desenvolvimento java, ele é responsável por **compilar** código-fonte (.java) em bytecode (.class)

# Questão 3

> Crie um programa Java que imprima o seguinte texto “Terminei a primeira aula com um programa Java!”.

Para acessar o programa Java desta questão, clique [aqui](https://github.com/ifpb-cz-ads/poo-2021-2-ac-01-team-pedroedwilson/blob/edwilson/PrimeiroPrograma.java).

# Questão 4

> Compile o programa desenvolvido no exercício anterior. A seguir apague o arquivo .class gerado e tente executar o programa. O que aconteceu?

Ele retorna um **error**, ao qual ele procura o arquivo compilado **.class**, mas não encontra, impedindo assim a sua execução.

Error retornado:

```
Não foi possível localizar nem carregar a classe principal PrimeiroPrograma
```

# Questão 5

> Mude o nome do método “main” para “start”, compile e execute. O que
aconteceu?

O interpretador **java** não encontra o método "main" e o terminal retorna o seguinte erro:

```
o método main não foi encontrado na classe PrimeiroPrograma; defina o método main como:
   public static void main(String[] args)
ou uma classe de aplicativo JavaFX deve expandir javafx.application.Application
```

# Questão 6

> Crie um programa Java para imprimir duas linhas de texto usando duas linhas de código “System.out”, onde aparecerá o seu nome na primeira linha e na segunda linha aparecerá o time para o qual você torce.

Atividade adicionada por meio do arquivo, para acessar o .java, clique [aqui](https://github.com/ifpb-cz-ads/poo-2021-2-ac-01-team-pedroedwilson/blob/Pedro/NomeMaisTime.java).

# Questão 7

> Experimente escrever todo o programa anterior em maiúsculo, compile e
execute. O que aconteceu?

Devido a linguagem Java ser **case-sensitive**, o que significa que nela ocorre uma diferenciação entre letras minúsculas e maiúsculas, o terminal retorna o seguinte erro:

```
NomeMaisTime.java:8: error: class, interface, enum, or record expected
CLASS NOMEMAISTIME {
^
NomeMaisTime.java:11: error: class, interface, enum, or record expected
        SYSTEM.OUT.PRINTLN("TIME QUE TORCE: FLAMENGO");
        ^
NomeMaisTime.java:12: error: class, interface, enum, or record expected
    }
    ^
3 errors
```

# Questão 8

> Experimente salvar o arquivo com um nome diferente do nome da classe, compile e execute. O que aconteceu?

Ao salvar o arquivo com um nome diferente ele compila normalmente, mas como resultado, temos apenas um arquivo com o nome dado a classe, tendo a extesão .class.

Ao tentarmos executar o nome do arquivo com a extensão .java, ele retornar o mesmo error dito na questão 4, mas se executarmos o arquivo com a extensão .class, ele rodará normalmente.

Digamos que tenhamos uma class com o nome HelloWorld:

```
class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!"); 
    }
}
```

E salvamos o arquivo como [OlaMundo.java](https://github.com/ifpb-cz-ads/poo-2021-2-ac-01-team-pedroedwilson/blob/Pedro/OlaMundo.java), ao compilarmos ele irá gerar um arquivo HelloWorld.class, ao qual será o arquivo executavel.

Ao tentarmos executar o **java OlaMundo** temos como resultado:

```
Erro: Não foi possível localizar nem carregar a classe principal OlaMundo
```

já ao tentarmos executar o **java HelloWorld** temos a execução normal do progama, nesse caso o resultado será:

```
Hello, World!
```
