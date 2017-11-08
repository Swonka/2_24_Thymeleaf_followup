# Delete

#### delete.html
````     
  // I denne demo af delete er der ingen html (view) side

````     

#### controller
````     
    @GetMapping("/delete")
    public String delete(@RequestParam("studentId") String studentId){
        studentRepository.delete(Integer.parseInt(studentId));
        return "redirect:/";
    }
````      

#### repository
````      
    public void delete(int id) {  
        jdbc.update("DELETE FROM students WHERE student_id='" + id + "'");
    }
````      
