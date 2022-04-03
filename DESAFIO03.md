# Desafio-03-IDS
Desafio 03 do Programa de Seleção da IDS
Programa para encontrar o maior número primo abaixo de um numero digitado pelo usuário obtido pela soma consecutiva dos números primos.

=========================================================================================

Passos para executar o programa em Java.
 1 - Salve o arquivo o programa em alguma Pasta do Windows.
 2 - Clique no botão Iniciar e digite cmd. Pressione ↵ Enter para abrir o "Prompt de Comando".
 3 - Verifique se o Java está instalado. Digite java -version na linha de comando. Se o Java estiver instalado, você verá uma mensagem mostrando qual a versão dele            está instalada. Se isso não acontecer, será necessário acessar o site do Java e baixar o Java Development Kit (JDK), que é gratuito e pode ser encontrado aqui:          http://www.oracle.com/technetwork/java/javase/downloads/index.html.
 4 - Vá até a pasta correta. Use o comando cd seguido pelo nome da pasta de destino para sair do diretório atual.
     Por exemplo, se você estiver no diretório C:\Users\Bob\Project e quiser acessar a pasta C:\Users\Bob\Project\TitanProject , digite cd TitanProject e pressione ↵          Enter. Para mostrar uma lista com todos os arquivos e pastas do diretório atual, digite dir no Windows ou ls no Mac e pressione ↵ Enter
 5 - Execute o programa. Digite java arquivo e pressione ↵ Enter. Lembre-se de que você deve trocar "arquivo" pelo nome do arquivo do seu programa.
     Após pressionar ↵ Enter, o programa deve rodar.
     
  
 ======================================================================================= 
  
  Tecnologias utilizadas:
  1 - Java\jdk1.8.0_311
  2 - Prompt de Comando do DOS.
  3 - Bloco de Notas
     
=======================================================================================
     
import java.util.Scanner;

public class NumPrimos
{

  public static void main ( String args[] )
  {
	int z, cont, nump, soma = 0;
	Scanner p = new Scanner(System.in);
	System.out.println("Digite um número");
	int n = Integer.parseInt(p.nextLine());
	int np[] = new int[n];
	int v = 0;
	z = 4;
	np[0] = 2;
	np[1] = 3;
	np[2] = 5;
	np[3] = 7;
	//incluir no vetor dos os numeros primos menores do numero digitado
	    for (int x=4; x < n; x++)
	    { if ((x !=0) && (x != 1) && (x % 2 != 0) && (x % 3 != 0) && (x % 5 != 0) && (x % 7 !=0))
	      { 
		np[z] = x;
		z++;
	      }
	     }
	     for (int y=z; y<=z; y--)
	     {	
		soma = 0;
		v =0;
		while (v <= z)
		{  
		 soma = soma + np[v];
		 v++;
		 if (soma == np[y])
		   break;
		}
		  if (soma == np[y] )
	          { 
		    System.out.println(np[y] + " Maior numero primo abaixo de " + n + " obtido pela soma consecutivas de numeros primos");
		    break;
		    
		  }
	       }
   }
}	   
