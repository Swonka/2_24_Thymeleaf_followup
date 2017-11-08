# Update

#### update.html
````     
        <form   th:action="@{/update}" method="post" th:object="${stu}">
        <input type="text" th:field="*{studentId}" />
        <input type="text" th:field="*{firstName}" />
        <input type="text" th:field="*{lastName}" />
        <input type="date" th:field="*{enrollmentDate}" />
        <input type="text" th:field="*{cpr}" />

        <input type="submit" value="Update" />

    </form>
````

#### controller

````   
    @GetMapping("/update")
    public String update(@RequestParam("studentId") String studentId, Model model)
    {
        model.addAttribute("stu", studentRepository.read(Integer.parseInt(studentId)));
        return "update";
    }
    
    @PostMapping("/update")
    public String update(@ModelAttribute Student stu)
    {
        studentRepository.update(stu);
        return "redirect:/";
    }
````    

#### repository
````     
    public void update(Student st) {
                
                jdbc.update("UPDATE students SET " +
                "first_name ='"+ st.getFirstName() +"' , " +
                "last_name='"+ st.getLastName() +"' ," +
                "enrollmentdate='"+ st.getEnrollmentDate() +"' ," +
                "cpr='"+ st.getCpr() +"' WHERE student_id = '"+ st.getStudentId() +"'");
    }
````    

