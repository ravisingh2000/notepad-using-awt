# notepad-using-awt

import java.awt.*;
import java.awt.event.*;

class myframe extends Frame implements ActionListener{
      Button a,b,c;
     TextArea area;
      Scrollbar i4;
  
      myframe(){
          this.setVisible(true);
          this.setTitle("Notepad");
          this.setSize(800,400);
    
          this.addWindowListener(new WindowAdapter(){
            public void windowClosing(WindowEvent ae){
                System.exit(0);
            }
       });
         area=new TextArea();
          this.add(area);
          MenuBar i=new MenuBar();
          Font f=new Font ("arial",Font.BOLD,40);
          this.setMenuBar(i);
     
          Menu j=new Menu("File");
          i.add(j);
          MenuItem j1=new MenuItem("New");
          MenuItem j2=new MenuItem("New Window");
          MenuItem j3=new MenuItem("Save");
          MenuItem j4=new MenuItem("Save As");   
          j1.addActionListener(this);
          j2.addActionListener(this);
          j3.addActionListener(this);
          j4.addActionListener(this);
          j.add(j1);
          j.add(j2);
          j.add(j3);
          j.add(j4);
          Menu k=new Menu("Edit");
          i.add(k);
          MenuItem k1=new MenuItem("New");
          MenuItem k2=new MenuItem("New Window");
          MenuItem k3=new MenuItem("Save");
          MenuItem k4=new MenuItem("Save As");   
          k1.addActionListener(this);
          k2.addActionListener(this);
          k3.addActionListener(this);
          k4.addActionListener(this);
          k.add(k1);
          k.add(k2);
          k.add(k3);
          k.add(k4);
          Menu m=new Menu("Format");
          i.add(m);
          MenuItem m1=new MenuItem("New");
          MenuItem m2=new MenuItem("New Window");
          MenuItem m3=new MenuItem("Save");
          MenuItem m4=new MenuItem("Save As");   
          m1.addActionListener(this);
          m2.addActionListener(this);
          m3.addActionListener(this);
          m4.addActionListener(this);
          m.add(m1);
          m.add(m2);
          m.add(m3);
          m.add(m4);
          Menu n=new Menu("View");
          i.add(n);
          MenuItem n1=new MenuItem("New");
          MenuItem n2=new MenuItem("New Window");
          MenuItem n3=new MenuItem("Save");
          MenuItem n4=new MenuItem("Save As");   
          n1.addActionListener(this);
          n2.addActionListener(this);
          m3.addActionListener(this);
          n4.addActionListener(this);
          n.add(n1);
          n.add(n2);
          n.add(n3);
          n.add(n4);
         
          
          
         
      }
      public void actionPerformed(ActionEvent e){
        String i=e.getActionCommand();
        if(i.equals("New")){
            area.setBackground(Color.pink);
            //repaint();
        }
        else{
            new myframe();
        } 
      }

    
}
class my{
    public static void main(String[] args) {
        myframe i=new myframe();
        
    }
}
