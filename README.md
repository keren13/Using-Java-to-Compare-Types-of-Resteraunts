Using-Java-to-Compare-Types-of-Resteraunts
==========================================
public interface Compareable
{
    
    int compareTo(Object g);
}
public class Driver
{
   

    /**
     * Constructor for objects of class Driver
     */
    public static void main (String args[]) 
    {
       fastFood McDonald = new fastFood(12,500,3); //numbers are put in x,y,z thus  Employees, Salary, Rating
       fiveStar Great = new fiveStar(25, 300, 25); //numbers are put in x,y,z thus Customers, Salary, menuOptions
     int result = Great.compareTo(McDonald);
     System.out.println(result); //if else value result is printed, displayed in terminal window
     
     
    }

    /**
     * An example of a method - replace this comment with your own
     * 
     * @param  y   a sample parameter for a method
     * @return     the sum of x and y 
     */
    public static int compareTo(fastFood G)
    {
       fiveStar Great = new fiveStar(25, 300, 25); //numbers are put in x,y,z thus Customers, Salary, menuOptions
     
       if(G.Salary <= Great.Salary) //if else statements used to compare shared interface, Salary
       return 0;
       else if(G.Salary < 0)
       return -1;
       else
       return 1;
    }
}
public class fiveStar  //designing the class fiveStar 
{


    int menuOptions; //instance variable created
    int Salary;      //instance variable that can be used for compareTo method is created
    int Customers;   //instance variable created 
   

    /**
     * Constructor for objects of class fastFood
     */
    public fiveStar(int x, int y, int z) //assigning local variable values to instance variables so that they can hod desired numbers
    {
        Customers = x;  //Customers holds x
        Salary = y;     //Salary holds y
        menuOptions = z; //menuOptions holds z 
    }

      }
      public class fastFood implements Compareable//designing class for fastFood
{
    int Employees;    //instance varibale Employees created
    private int Salary;       //instance varibale Salary created so that it can be used for the compareTo method 
    int Rating;       //instance variable Rating  
   

    /**
     * Constructor for objects of class fastFood
     */
    public fastFood(int x, int y, int z) //assigning local variable values to instance variables so that they can hod desired numbers
    {
        Employees = x; //Employees holds x
        Salary = y;    //Salary holds y
        Rating = z;    //Rating holds z
    }

    public int compareTo(Object G)
    {
            
       if(this.Salary < G.Salary) //if else statements used to compare shared interface, Salary
       return -1;
       else if(this.Salary > G.Salary)
       return 1;
       else
       return 0;
    }
}


