# The-stone-that-the-builderman-rejected
//the login page of the company
package projectmanagement;
import javax.swing.*;
 import java.awt.FlowLayout;
import java.sql.Connection;


public class Projectmanagement extends JFrame {

   private JFrame fram;
    private JPanel pan;
    private JButton but1;
    private JButton but2;
    private JLabel lab1;
    private JLabel lab2;
    private JTextField text1;
    private JPasswordField texxt2;
     
   
        Connection conn=null;
    public Projectmanagement()
    { 
        gui();
        
    }
    public final void gui()
    {
         
            fram=new  JFrame("WELCOME USERS");
            fram.setVisible(true);
            fram.setSize(600,400);
            fram.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
           
            pan= new JPanel(new FlowLayout());
         
            
            pan.setLayout(null);
            but1= new JButton("EXIT");           
             but2= new JButton("LOGIN");                     
             lab1= new JLabel("USERNAME");
             lab2=new JLabel("PASSWORD");
             text1= new JTextField (10); 
             texxt2= new JPasswordField(10);
               pan.add(but1);
             pan.add(but2);
             pan.add(lab1);
             pan.add(lab2);
             pan.add(text1);
             pan.add(texxt2);
             fram.add(pan);
             
             lab1.setBounds(40,40,120,40);
             lab2.setBounds(40,70,120,40);
             but1.setBounds(40,120,100,30);
             but2.setBounds(150,120,100,30);
             text1.setBounds(200,40,200,30);
             texxt2.setBounds(200,70,200,30);
             
             
              but2.addActionListener((java.awt.event.ActionEvent evt)-> {
                but2ActionPerformed(evt);
    });
    }
    public void but2ActionPerformed(java.awt. event.ActionEvent evt ){
       String usname = text1.getText();
       String pass = texxt2.getText();
        
       
       if (usname.equals("null")&& pass.equals("null")){
           options b1= new options ();
       }
                  
       
       else  {
           JOptionPane.showMessageDialog(null,"Wrong Password/ Username . Try again");
           
           text1.setText("");
           texxt2.setText("");     
       }
    }

   public static void main(String[] args) {
      Projectmanagement b =  new Projectmanagement ();
   }
}
         
    
/*Here the users will now choose whether they are customers or if they are project managers*/
package projectmanagement;
import java.awt.FlowLayout;
import javax.swing.JButton;
import javax.swing.JFrame;
import javax.swing.JPanel;

public class options extends JFrame {
   
private JFrame frame;
private JPanel panel;
private JButton button1;
private JButton button2;    
    
public options()
    { 
      gui();
        
    }
public final void gui()
    {
         

    frame=new  JFrame("how may we help");
    frame.setVisible(true);
    frame.setSize(600,400);
    frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
           
    panel= new JPanel(new FlowLayout());
         
            
    panel.setLayout(null);
    button1= new JButton("CUSTOMER");           
    button2= new JButton("PROJECT MANAGER");  
             
             
    panel.add(button1);
    panel.add(button2);
    frame.add(panel);
             
    button1.setBounds(150,120,100,30);
    button2.setBounds(150,170,100,30);
     
       }
public static void main(String[] args) {
      options b =  new options();
}       
}
    

