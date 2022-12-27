package group;
import java.io.*;
import java.util.*;
public class Group {

static Scanner input = new Scanner(System.in) ; 

public static void main(String[] args) {
    ArrayList<Student> list = new ArrayList<Student>(); 
    int choice = 0 ; 
    System.out.println("Welcom to CS102 Lab project ");
    while( choice != 7 ){
        System.out.println("To read students data from a file, please enter 1 ");
        System.out.println("To search for a student record, please enter 2 ");
        System.out.println("To sort the students data , please enter 3 ");
        System.out.println("To update a student record, please enter 4 ");
        System.out.println("To delete a student record, please enter 5 ");
        System.out.println("To save the students data, please enter 6 ");
        System.out.println("to exit the program, please enter 7 ");
            System.out.println("Please enter your choice: ");

    choice = input.nextInt(); 
        switch(choice){
    case 1 : 
        try{
        Scanner file = new Scanner(new File("C:/Users/naure/OneDrive/Desktop/Students_Records.txt")) ; 
            while(file.hasNext()){
                int id = file.nextInt(); 
                Name name = new Name(file.next() , file.next() , file.next() ) ; 
                String major = file.next() ; 
                double gpa = file.nextDouble(); 
                int hr = file.nextInt(); 
                Student st = new Student(id , name , major , gpa , hr ) ; 
l               ist.add( st ) ; 
                    }// end while hasNext
        System.out.println("read from file is done");
        file.close(); 
        }catch(IOException ex ){
                System.out.println("error while file open and read from file");
}
    for(Student s:list){
    System.out.println(s);
}
        break; 
        case 2 : 
        Search(list) ; // calling to method
        break; 
        case 3 : 
        sort(list); // calling to method 
        break; 
        case 4 : 
        System.out.print("Enter id ");
        int id = input.nextInt(); 
            boolean found = false; 
            for(Student S : list )
            if( S.getId() == id ){
                found = true;
    System.out.println("Enter new Full name (first , Middel , last ) : "); 
    Name nameObj = new Name(input.next() ,input.next() ,input.next() ) ; 
    S.setFullName(nameObj);
    System.out.print("Enter new GPA : ");
    double gpa = input.nextDouble(); 
    S.setGpa(gpa);
    System.out.print("Enter new Major : " ) ; 
    String major = input.next(); 
    S.setMajor(major);
    System.out.print("Enter complete credit hours ");
    int hr = input.nextInt(); 
    S.setHours(hr);
    System.out.println("update done \n ");
}
    if( found == false )
        System.out.println("this id not found");
        break; 
        case 5 : 
        System.out.print("Enter id ");
        int id2 = input.nextInt(); 
        boolean found1 = false; 
        for(Student S : list )
        if( S.getId() == id2 ){
        found1 = true;
        list.remove(S) ; 
        System.out.println("delet done.");
        break; // out from loop
}
    if( found1 == false)
        System.out.println("this id not found");
            break; 
            case 6 :
            try{
                PrintWriter output= new PrintWriter(new File("info.txt")) ; 
                for( Student S : list )
                output.println(S.toString());
                output.close();
                System.out.println("save all record to file is done. \n");
}   catch(IOException ex){
        System.out.println(ex.toString() );
}
        break; 
        case 7 : 
        System.exit(0);
        break; 
        default : 
        System.out.println("invalid input") ; 
} // end of switch
}// end of while
}// end of main 
//=======================
public static void search(ArrayList<Student> list ){
    System.out.println("enter your choice to search : ");
    System.out.println("1- search with id ");
    System.out.println("2- search with Name ");
    System.out.println("3- search with Gpa ");
    System.out.println("4- search with major ");
    System.out.println("5- search with Completed credit hours ");
    int ch = input.nextInt(); 
    switch(ch){
        case 1 : 
        System.out.print("Enter id ");
        int id = input.nextInt(); 
        for(Student S : list )
            if( S.getId() == id ){
                System.out.println(S.toString());
                return ; 
}
                System.out.println("Not found");
        break; 
        case 2 : 
        System.out.print("Enter first Name , middle Name , last Name ");
        Name name = new Name(input.next() , input.next() , input.next() ) ; 
        for(Student S : list )
            if( S.getFullName().compareTo(name) == 0 ){
                System.out.println(S.toString());
        return ; 
}
        System.out.println("Not found");
        break; 
        case 3 : 
        System.out.print("Enter Gpa ");
        double gpa = input.nextDouble() ; 
        for(Student S : list )
        if( S.getGpa() == gpa ){
            System.out.println(S.toString());
        return ; 
}
        System.out.println("Not found");
        break; 
        case 4 : 
        System.out.print("Enter major ");
        String major = input.next(); 
        for(Student S : list ) 
            if( S.getMajor().equals(major) ){
            System.out.println(S.toString());
        return ; 
}
        System.out.println("Not found");
        break; 
        case 5 :
        System.out.print("Enter completed credit hours ");
        int hr = input.nextInt() ; 
        for(Student S : list )
            if( S.getHours() == hr ){
                System.out.println(S.toString());
        return ; 
}
        System.out.println("Not found");
        break; 
        default : 
        System.out.println("invalid input ") ; 
}// end of switch
}// end of method search
//========================================================
public static void sort(ArrayList<Student> list ){
    System.out.println("enter your choice to search : ");
    System.out.println("1- sort based on id ");
    System.out.println("2- sort based on Name ");
    System.out.println("3- sort based on Gpa ");
    System.out.println("4- sort based on major ");
    System.out.println("5- sort based on Completed credit hours ");
    int choice = input.nextInt(); 
switch(choice){
case 1 : 
Collections.sort(list);
break; 
case 2 : 
Collections.sort(list , new NameComp() ) ; 
break; 
case 3 : 
Collections.sort(list , new GpaComp() ) ; 
case 4 : 
Collections.sort(list , new MajorComp() ) ; 
break; 
case 5 :
Collections.sort(list , new HoursComp() ) ; 
break; 
default : 
System.out.println("invalid input ") ; 
return ; 
}// end switch
for( Student S : list)
System.out.println(S.toString());
}// end mthod sort
//==============================================
}
