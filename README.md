# atividade-Z   
import java.util.Scanner;

public class Execicio {
	
	public static void main(String[] args) {
	    String alfabeto = "ABCDEFGHIJKLMNOPQRSTUVXWYZ";
	    char vetorAlfabeto[] = alfabeto.toCharArray();
	    System.out.println("escolhar o numero da Matrix linha ");
	    int matrixlinha = new Scanner(System.in).nextInt();
	    System.out.println("escolhar o numero da  Matrix Colunas: ");
	    int matrixColuna = new Scanner(System.in).nextInt();
	    int contAlfabeto=0,contMatrizLinha=1,contMatrizColuna=matrixColuna-2;

	    
	    if (matrixlinha > 50 && matrixColuna > 50) {
	        System.out.print("ERROR");
	    }
	    if (matrixlinha != matrixColuna) {
	        System.out.print("ERROR");
	    }
	    if (matrixlinha < 3 && matrixColuna < 3) {
	        System.out.print(" ERROR");
	    }

	    char[][] matrix = new char[matrixlinha][matrixColuna];
	    for(int i=0;i<matrixlinha;i++){
	        for(int j=0;j<matrixlinha;j++){
	            matrix[i][j]=' ';
	        }
	    }
	    for(int i=0;i<matrixColuna;i++){
	        matrix[0][i]=vetorAlfabeto[contAlfabeto];
	        contAlfabeto++;
	        if(contAlfabeto==26){
	            contAlfabeto=0;
	        }
	    }
	    for(;(contMatrizLinha+1)<matrixlinha;contMatrizLinha++,contMatrizColuna--){
	        matrix[contMatrizLinha][contMatrizColuna]=vetorAlfabeto[contAlfabeto];
	        contAlfabeto++;
	        if(contAlfabeto==26){
	            contAlfabeto=0;
	        }
	    }
	    contMatrizLinha=matrixlinha-1;
	    for(int i=0;i<matrixColuna;i++){
	        matrix[contMatrizLinha][i]=vetorAlfabeto[contAlfabeto];
	        contAlfabeto++;
	        if(contAlfabeto==26){
	            contAlfabeto=0;
	        }
	    }
	    for(int i=0;i<matrixlinha;i++){
	        for(int j=0;j<matrixColuna;j++){
	            System.out.print(matrix[i][j]+"   ");
	        }
	        System.out.println();
	    }
	}
	}
