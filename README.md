# check
checking
import java.util.Scanner;
public class check
{
	public static Scanner reader = new Scanner(System.in);
	public static void main(String[] args)  
	{
		String abc;
		int counterNum=0,counterOt=0,counterSof=0;
		System.out.println("Enter String");
		abc=reader.next();
		for (int i=0;i<abc.length();i++)
		{	
			for (int j='A';j<='z';j++)
			{
				if(j==91)
				{
					j=97;
				}
				if (abc.charAt(i)==j)
				{
					counterOt++;
				}
				else if(abc.charAt(i)<=9)
				{
					counterNum++;
				}
			}
			if (counterNum>0&&counterOt>0)
			{
				if(abc.length()>=6)
				{
					counterSof++;
				}
			}
			if(i==(abc.length()-1))
			{
				if(counterSof<6)
				{
					System.out.println("Bad password, Try again");
					abc=reader.next();
					i=0;
				}
			}
		}
		if(counterSof>=6)
			System.out.println("good password!");
	}
}
