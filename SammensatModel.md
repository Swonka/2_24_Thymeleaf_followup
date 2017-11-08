Tit vil i have brug for at kunne skrive noget ind i en html form hvor der er mere data end hvad der er plads til i en entity (class).

Et eksempel:

````     
  public class Student {

    private int studentId;
    private String firstName;
    private String lastName;
    @DateTimeFormat(pattern = "yyyy-MM-dd")
    private Date enrollmentDate;
    private String cpr;
    
    // Getters & Setters ....
}
````    
  
````     
  public class Course {

    private int courseId;
    private String title;
    private String etcs;
    
    // Getters & Setters ....
}
````   
