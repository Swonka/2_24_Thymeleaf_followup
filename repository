# Repository

#### Interface
````     
  public interface ICrudRepository<T> {

    public void create(T t);
    
    public ArrayList<T> readAll();
    
    public T read(int id);
    
    public void update(T t);
    
    public void delete(int id);

}
````     

#### repository

````    
  @Repository
  public class StudentRepository implements ICrudRepository<Student> {

    @Autowired
    private JdbcTemplate jdbc;
    
    // impemented methods here ...
    
````    

