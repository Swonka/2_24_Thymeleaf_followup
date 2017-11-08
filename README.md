# Dag 24 Thymeleaf, html og overførelse af data - followup
Agenda dag 24 d. 9-11-2017

````      
    <form th:action="@{/create}" method="post" th:object="${student}"> <!-- student = @ModelAttribute -->

        <input type="text" th:field="*{firstName}" />
        <input type="text" th:field="*{lastName}" />
        <input type="date" th:field="*{enrollmentDate}" />
        <input type="text" th:field="*{cpr}" />

        <input type="submit" value="Send" />

    </form>
````    

## Tutorial
* [The Thymeleaf Interactive Tutorial](http://itutorial.thymeleaf.org/)
