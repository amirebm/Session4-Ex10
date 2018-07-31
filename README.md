// برنامه ایی بنویسید که ماتریسی گرفته و ترانهاده آن را محاسبه نماید

# Session4-Ex10
package com.personal.Ex10;

import java.util.Scanner;

public class Ex10 {

	static Scanner sc;
	static int dimM,dimN;
	static int[][] TranposedMatrix;
	

	public static void main(String[] args) {
		
		
		System.out.println("Enter a the size of matrixes of 2d");
		System.out.println("Enter a the first dimention of matrixes");
		sc= new Scanner(System.in);
		dimM=sc.nextInt();
		System.out.println("Enter a the second dimention of matrixes");
		dimN=sc.nextInt();
		int[][] arX= new int[dimM][dimN];
		int[][] arY= new int[dimM][dimN];
		
		System.out.println("Please enter the values of the  matrix:");
		System.out.println("*****************************");
		System.out.println("it should be: "+ dimM*dimN +"  Numbers");
		
		AddToMatrix(arX, dimM, dimN);
		


		System.out.println("The value of the Orignal Matrix is :");

		printMatrix(arX,dimM,dimN);
		System.out.println("The value of the Orignal Matrix which is transpoed  :");
		transposeMatrix(arX, dimM, dimN);
		printMatrix(TranposedMatrix,dimN,dimM);

			}
	
    static void transposeMatrix(int[][] arrX,int dimM, int dimN) {
    	
    	TranposedMatrix= new int[dimN][dimM];
        for (int i = 0; i < dimM; i++) {
			
			for (int j = 0; j < dimN; j++) {
			
				TranposedMatrix[j][i]=arrX[i][j];
				
			}
			
		}
    	
    }

    static void AddToMatrix(int[][] arr, int dimM, int dimN) {
        for (int i = 0; i < dimM; i++) {
			
			for (int j = 0; j < dimN; j++) {
			
				arr[i][j]=sc.nextInt();
			}
			
		}
        
       	}
	static void printMatrix(int arr[][],int m, int n)
	{

	    for (int i=0; i<m; i++) {
	    	for (int j = 0; j < n; j++) {
	    		 System.out.print(String.format("[%d][%d]=%d\t", i, j,arr[i][j]));	
			}
	       
	    System.out.println();
	    }
	}
}
