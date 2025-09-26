import java.util.*;// All classes are imported
public class otp_generator {

	public static void main(String[] args) {
		Scanner nil = new Scanner(System.in);
		Random random= new Random();// finding a random value
		long r;//Storing the random value
		System.out.println("Enter the number of digits  in the \"OTP\" =");
	    int n= nil.nextInt();//asking the number of digits in otp
		//for checking 0
		char ch = 'x';
		while(ch!='y') {
		    
		    if (n>0) {
		    	ch='y';
		    	
		    }
		    else {
		    	System.out.println("Re-enter the value in non zero ");
		    	n=nil.nextInt();
		    }
		}
		// calculating max and min for random limits
		int max=0,min=0;
		for(int i=0;i<=n-1;i++) {
			max += 9*Math.pow(10, i);
			min += 1*Math.pow(10, i);
		}
		//max and min value is stored
		r= random.nextInt(max-min+1)+min;
		//random value is out now
		System.out.println("The \"OTP\" is "+r);	
			}
		}
		
