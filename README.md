# Reverse-word-from-particular-character
import java.util.Scanner;

public class VasyErp
{
   public void reverseWordInMyString(String str)
   {
	String[] words = str.split(" ");
	String reversedString = "";
	
	
	  Scanner sc = new Scanner(System.in);
      System.out.println("Enter the /characters do you want to skip in word" );
      
      int count = sc.nextInt();
	for (int i = 0; i < words.length; i++)
	{
           String word = words[i]; 
           String reverseWord = "";          
           for ( int j = word.length()-1; j >= count; j--){
		reverseWord =  reverseWord +  word.charAt(j) ;	
	   }
//           HERE IT ADDS THE leftover characters to the revsersed string
       reverseWord = word.substring(0, count)+ reverseWord;             
	   reversedString =  reversedString + reverseWord + " ";
	}	
	System.out.println(str);
	System.out.println( reversedString);
   }
   
   public static void main(String[] args) 
   {
	   
	VasyErp obj = new VasyErp();
	
	Scanner sc = new Scanner(System.in);
	
	System.out.println("Enter the string from which you want to reverse its words from particular character");
	obj.reverseWordInMyString(sc.nextLine());

   }
}
