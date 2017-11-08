# Create
##### create.html
````      
    <form th:action="@{/create}" method="post" th:object="${student}">

        <input type="text" th:field="*{firstName}" />
        <input type="text" th:field="*{lastName}" />
        <input type="date" th:field="*{enrollmentDate}" />
        <input type="text" th:field="*{cpr}" />

        <input type="submit" value="Send" />

    </form>
````    
##### controler
````     
    @GetMapping("/create")
    public String create(Model model) {
        model.addAttribute("student", new Student());
        return "create";
    }

    @PostMapping("/create")
    public String create(@ModelAttribute Student stu){

        studentRepository.create(stu);
        return "redirect:/";
    }
````     
#### repository

````     
public void create(Student st) {
        jdbc.update("insert into students(first_name,last_name, enrollmentdate, cpr)values('Claus666','Bove', '2010-10-10', '221070-3333')");
    }
````

