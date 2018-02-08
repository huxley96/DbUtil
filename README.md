package DbUtil;
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.SQLException;

public class dbconnection {
    private static final String username = "username";
    private static final String password = "password";
    private static final String  OONN = "jdbc:mysql://localhost/login";
    private static final String SCONN = "jdbc:sqlite:stany.sqlite";

    public static Connection getConnection()throws SQLException{

        try{
            System.out.println("Tutaj wchodze dbconneciton");
            Class.forName("org.sqlite.JDBC");
            return DriverManager.getConnection(SCONN);
        }catch (ClassNotFoundException ex){
            System.out.println("Tutaj wchodze dbconneciton catch");
            ex.printStackTrace();
        }
        return null;
    }
}
