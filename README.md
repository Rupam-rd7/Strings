# Strings
//Count the number of odd and even charactered words in a sentence

import java.util.Scanner;

public class Main
{
	public static void main(String[] args) 
	{
		int f=0; //points to the start of word
		int even=0; //counts even words
		int odd=0; //counts odd words
		System.out.println("Enter the string");
		Scanner sc = new Scanner(System.in);
		String s1= sc.nextLine();
		char[] c1= s1.toCharArray();
		for(int i=0; i<c1.length;i++)
		{
			if(c1[i]==' ' && c1[i+1]!=' ')
			{
				int k= i-f; //length of word
				f= i+1;
				if(k%2==0)
					even++;
				else
					odd++;	
			}
			if(i==c1.length-1)
			{
				int k= i-f+1;
				if(k%2==0)
					even++;
				else
					odd++;
			}
		}
		System.out.println("Number of even words: "+even);
		System.out.println("Number of odd words: "+odd);
	}
}
