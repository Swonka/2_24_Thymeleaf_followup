# Dag 24 Thymeleaf, html og overførelse af data - followup
Agenda dag 24 d. 9-11-2017

#### Create
##### create.html
````      
    <form th:action="@{/create}" method="post" th:object="${student}"> <!-- student = @ModelAttribute -->

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



## Tutorial
* [The Thymeleaf Interactive Tutorial](http://itutorial.thymeleaf.org/)
