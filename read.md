# Read
#### index.html
````     
  <table>
    <tr>
        <td>ID</td>
        <td>First Name</td>
        <td>Last Name</td>
        <td>Enrollment Date</td>
        <td>Cpr</td>
        <td>Knapper</td>
    </tr>
    <tr th:each="student: ${stu}">
        <td th:text="${student.studentId}"/>
        <td th:text="${student.firstName}"/>
        <td th:text="${student.lastName}"/>
        <td th:text="${student.enrollmentDate}"/> 
        <td th:text="${student.cpr}"/>
        
        <td><a th:href="@{/details(studentId=${student.studentId})}" class="btn" id="blue">DETAILS</a>
            <a th:href="@{/delete(studentId=${student.studentId})}" class="btn" id="blue">DELETE</a></td>
    </tr>
</table>
````    

#### controller
````     
    // READ ALL
    @GetMapping("/")
    public String index(Model model) {
        students = studentRepository.readAll();
        model.addAttribute("stu", students);
        return "index";
    }
````     
#### repository
````     
  public ArrayList<Student> readAll() {

        rs = jdbc.queryForRowSet("select * from students");
        
        while (rs.next()) {
            students.add(new Student(rs.getInt("student_id"),
                    rs.getString("first_name"),
                    rs.getString("last_name"),
                    rs.getDate("enrollmentdate"),
                    rs.getString("cpr")));
        }
        
        return students;
    }
````     
