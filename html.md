# Html og thymeleaf form elements examples

## The ```` <input> ````  Element

### text
````    
  <input name="firstname" type="text">
  
  <input type="text" th:field="*{firstname}">

````   
### radio
````    
  <input type="radio" name="gender" value="male" /> Male<br />
  <input type="radio" name="gender" value="female" /> Female<br />
  <input type="radio" name="gender" value="other" /> Other <br />
  
  When a user clicks on a radio-button, it becomes checked, and all other radio-buttons with equal name become unchecked.

````    
