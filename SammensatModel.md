Tit vil i have brug for at kunne skrive noget ind i en html form hvor der er mere data end hvad der er plads til i en entity (class) og en tabel i databasen.

Et eksempel:
i Har en Company Class
````     
  public class Company {

    private int companyId;
    private String name;
    
    // Getters & Setters ....
}
````    

Og en Employee Class
  
````     
  public class Employee {

    private int employeeId;
    private String jobTitle;
    private String email;
    
    // Getters & Setters ....
}
````   
Når der oprettes en ny virksomhed skal der tilknyttes en kontaktperson til virksomheden ved oprettelsen. Derfor har i brug for at overføre data som har med begge klasser at gøre.    

I dette tilfælde ville jeg lave en ny entity, eller noget man kunne kalde en sammensat entity.    

````     
  public class CompanyEmployee {

    private Company company;
    private Employee employee;
    
    // Getters & Setters ....
}
````   
