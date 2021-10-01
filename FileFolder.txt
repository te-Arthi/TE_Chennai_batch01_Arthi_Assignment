package com.aa.folder.c;
import java.util.Scanner;
import java.io.File;
import java.io.FileWriter;
import java.io.IOException;

public class FolderCreate {

	public static void main(String[] args) {
		File ma = new File("D:\\Amu");

		ma.mkdir();

		File ref = new File("D:\\Amu\\arthi.txt");
		try {
			ref.createNewFile();
		} catch (IOException e) {
			e.printStackTrace();
		}
		try {
			FileWriter obj = new FileWriter(ref);
			obj.write("Hello Iam Arthi!!!!!");
			obj.flush();
			
		} catch (IOException e) {
						e.printStackTrace();
		}
		 try { 
			  File sal=new File("D:\\Amu\\arthi.txt"); 
			  Scanner scanner = new Scanner(sal); 
			  while (scanner.hasNext()) { 
			   System.out.println(scanner.nextLine()); 
			   scanner.close(); 
			  } 
			 } catch (Exception b) { 
			   
			 }
		 
		 
	}

}
