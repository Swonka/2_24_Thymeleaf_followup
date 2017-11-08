# Update

#### update.html
````     

````

#### controller

````   

````    

#### repository
````     
    public void update(Student st) {
        int result = jdbc.update("UPDATE students SET " +
                "first_name ='"+ st.getFirstName() +"' , " +
                "last_name='"+ st.getLastName() +"' ," +
                "enrollmentdate='"+ st.getEnrollmentDate() +"' ," +
                "cpr='"+ st.getCpr() +"' WHERE student_id = '"+ st.getStudentId() +"'");
    }
````    

