import java.awt.*;
import javax.swing.*;
import java.awt.event.*;
public class mycalculator implements ActionListener {
	
	int c,n;
	String s1,s2,s3,s4,s5;
	JFrame f;
	JButton b1,b2,b3,b4,b5,b6,b7,b8,b9,b10,b11,b12,b13,b14,b15,b16,b17,b18,b19,b20;
	Panel p;
	JTextField tf;
	//GridLayout g;	
	
	//		CONSTRUCTOR		......
	
	mycalculator(){		
		
		f=new JFrame("  MY  CALCULATOR  ");
		p=new Panel();
		f.setLayout(null);		
		
		//		DECLARING 	  HEADING   ......		
		
		JLabel l_first_head=new JLabel(" JAVA ");
		JLabel l_sec_head=new JLabel(" SIMPLE  CALCULATOR ");
		JLabel myname=new JLabel(" :  Purusharth Sharma ");		
		
		//		INITIALISING	   BUTTONS   ......		
		
		b1=new JButton(" 0 ");			b1.addActionListener(this);
		b2=new JButton(" 1 ");			b2.addActionListener(this);
		b3=new JButton(" 2 ");			b3.addActionListener(this);
		b4=new JButton(" 3 ");			b4.addActionListener(this);
		b5=new JButton(" 4 ");			b5.addActionListener(this);
		b6=new JButton(" 5 ");			b6.addActionListener(this);
		b7=new JButton(" 6 ");			b7.addActionListener(this);
		b8=new JButton(" 7 ");			b8.addActionListener(this);
		b9=new JButton(" 8 ");			b9.addActionListener(this);
		b10=new JButton(" 9 ");			b10.addActionListener(this);		
		b11=new JButton(" + ");			b11.addActionListener(this);
		b12=new JButton(" - ");			b12.addActionListener(this);
		b13=new JButton(" * ");			b13.addActionListener(this);
		b14=new JButton(" / ");			b14.addActionListener(this);
		b15=new JButton(" % ");			b15.addActionListener(this);		
		b16=new JButton(" . ");			b16.addActionListener(this);
		b17=new JButton(" = ");			b17.addActionListener(this);
		b18=new JButton(" C ");			b18.addActionListener(this);
		b19=new JButton(" AC ");		b19.addActionListener(this);
		b20=new JButton(" OFF ");		b20.addActionListener(this);		
		
		//		DECLARING	TEXTFIELD	......		
		
		tf=new JTextField(26);		
		
		
		//		DECLARING	   FONT	 OF		DIFFERENT 	FIELDS	......		
		
		Font head = new Font("Arial",Font .BOLD,30);		//	HEADING	...
		Font text = new Font("Arial",Font.BOLD,19);			//	TEXT	FIELD ...
		Font off = new Font("Arial",Font.BOLD,15);			//	MAIN	BUTTON ...
		Font flc = new Font("Arial",Font.BOLD,13);			//	ALL		BUTTON ...
		Font fop = new Font("Arial",Font.BOLD,11);			//	'%'		BUTTUON ...
		Font 	my_name = new Font("Arial",Font.ITALIC,14);			//	MYNAME		HEADING ...		
		
		
		//		SETTING	UP	OF	BOUNDS	OF	ALL	FIELDS	......				
		
		l_first_head.setBounds(130,5,180,50);
		l_sec_head.setBounds(70,50,240,40);
		tf.setBounds(60,110,250,40);
		b1.setBounds(60,400,50,30);
		b18.setBounds(230,190,78,30);
		b16.setBounds(125,400,50,30);
		b11.setBounds(255,400,50,30);
		b2.setBounds(60,350,50,30);
		b3.setBounds(125,350,50,30);
		b4.setBounds(190,350,50,30);
		b12.setBounds(255,362,50,30);
		b5.setBounds(60,300,50,30);
		b6.setBounds(125,300,50,30);
		b7.setBounds(190,300,50,30);
		b13.setBounds(255,325,50,30);
		b8.setBounds(60,250,50,30);
		b9.setBounds(125,250,50,30);
		b10.setBounds(190,250,50,30);
		b14.setBounds(255,288,50,30);
		b15.setBounds(255,250,50,30);
		b19.setBounds(145,190,78,30);
		b17.setBounds(190,400,50,30);		
		b20.setBounds(60,190,78,30);
		myname.setBounds(235,450,150,30);
		
		
		//		SETTING		COLORS		OF		DIFFERENT		FIELDS	......
		
		
		b19.setBackground(Color.gray);
		b17.setBackground(Color.gray);
		b20.setBackground(Color.RED);
		b16.setBackground(Color.lightGray);
		b11.setBackground(Color.lightGray);
		b12.setBackground(Color.lightGray);
		b13.setBackground(Color.lightGray);
		b14.setBackground(Color.lightGray);
		b15.setBackground(Color.lightGray);
		b18.setBackground(Color.gray);		
		
		
		//		SETTING		FONTS		OF		DIFFERENT		FIELDS	......		
		
		l_first_head.setFont(head);
		l_sec_head.setFont(text);
		tf.setFont(text);
		b1.setFont(flc);
		b2.setFont(flc);
		b3.setFont(flc);
		b4.setFont(flc);
		b5.setFont(flc);
		b6.setFont(flc);
		b7.setFont(flc);
		b8.setFont(flc);
		b9.setFont(flc);
		b10.setFont(flc);
		b11.setFont(flc);
		b12.setFont(flc);
		b13.setFont(flc);
		b14.setFont(flc);
		b15.setFont(fop);
		b16.setFont(flc);
		b17.setFont(flc);
		b18.setFont(off);
		b19.setFont(off);
		b20.setFont(off);
		myname.setFont(my_name);		
		
		
		//		ADDING		ALL		FIELDS		TO		FRAME	......		
		
		f.add(l_first_head);
		f.add(l_sec_head);
		f.add(tf);
		f.add(b1);
		f.add(b2);
		f.add(b3);
		f.add(b4);
		f.add(b5);
		f.add(b6);
		f.add(b7);
		f.add(b8);
		f.add(b9);
		f.add(b10);
		f.add(b11);
		f.add(b12);
		f.add(b13);
		f.add(b14);
		f.add(b15);
		f.add(b16);
		f.add(b17);
		f.add(b18);
		f.add(b19);
		f.add(b20);		
		f.add(myname);
		
		f.add(p);
		f.setSize(400,520);
		f.setVisible(true);
		
	}
	
	
	
	//		IMPLEMENTS	ACTION	TO	BUTTONS	......
	
	
	public void actionPerformed(ActionEvent e){
		
		
		//		DISPLAY		'0'		FOR	B1	... 
		
		if(e.getSource()==b1){
			s3=tf.getText();
			
			s4="0";
			s5=s3+s4;
			tf.setText(s5);
		}
		
		
		//		DISPLAY		'1'		FOR	B1	...
		
		if(e.getSource()==b2){
			s3=tf.getText();
			s4="1";
			s5=s3+s4;
			tf.setText(s5);
		}
		
		
		//		DISPLAY		'2'		FOR	B1	...
		
		if(e.getSource()==b3){
			s3=tf.getText();
			s4="2";
			s5=s3+s4;
			tf.setText(s5);
		}
		
		
		//		DISPLAY		'3'		FOR	B1	...
		
		if(e.getSource()==b4){
			s3=tf.getText();
			s4="3";
			s5=s3+s4;
			tf.setText(s5);
		}
		
		
		//		DISPLAY		'4'		FOR		B5	...
		
		if(e.getSource()==b5){
			s3=tf.getText();
			s4="4";
			s5=s3+s4;
			tf.setText(s5);
		}
		
		
		//		DISPLAY		'5'		FOR	B1	...
		
		if(e.getSource()==b6){
			s3=tf.getText();
			s4="5";
			s5=s3+s4;
			tf.setText(s5);
		}
		
		
		//		DISPLAY		'6'		FOR	B1	... 
		
		if(e.getSource()==b7){
			s3=tf.getText();
			s4="6";
			s5=s3+s4;
			tf.setText(s5);
		}
		
		
		//		DISPLAY		'7'		FOR	B1	... 
		
		if(e.getSource()==b8){
			s3=tf.getText();
			s4="7";
			s5=s3+s4;
			tf.setText(s5);
		}	
		
		
		//		DISPLAY		'8'		FOR	B1	... 
		
		if(e.getSource()==b9){
			s3=tf.getText();
			s4="8";
			s5=s3+s4;
			tf.setText(s5);
		}
		
		
		//		DISPLAY		'9'		FOR	B1	... 
		
		if(e.getSource()==b10){
			s3=tf.getText();
			s4="9";
			s5=s3+s4;
			tf.setText(s5);
		}
		
		
		
		//		SET		C=1		WHEN	'+'		IS		ACTIVATED	...
		
		if(e.getSource()==b11){
			s1=tf.getText();
			tf.setText("");
			c=1;
		}
		
		
		//		SET		C=2		WHEN	'+'		IS		ACTIVATED	...
		
		if(e.getSource()==b12){
			s1=tf.getText();
			tf.setText("");
			c=2;
		}
		
		
		//		SET		C=3		WHEN	'-'		IS		ACTIVATED	...
		
		if(e.getSource()==b13){
			s1=tf.getText();
			tf.setText("");
			c=3;			
		}
		
		
		//		SET		C=4		WHEN	'*'		IS		ACTIVATED	...
		
		if(e.getSource()==b14){
			s1=tf.getText();
			tf.setText("");
			c=4;
		}
		
		
		//		SET		C=5		WHEN	'/'		IS		ACTIVATED	...
		
		if(e.getSource()==b15){
			s1=tf.getText();
			tf.setText("");
			c=5;
		}		

		
		//		DISPLAY		'.'		...
		
		if(e.getSource()==b16){
			s3=tf.getText();
			s4=".";
			s5=s3+s4;
			tf.setText(s5);
		}
		
		
		
		//		PERFORMED	CERTAIN		OPERATION		WHEN		'='		IS		PRESSED	...
		
		if(e.getSource()==b17){
			s2=tf.getText();
			
			//		ADDITION	...
			if(c==1){
				n=Integer.parseInt(s1)+Integer.parseInt(s2);
				tf.setText(String.valueOf(n));
			}
			else
				
				//		SUBTRACTION		...
				if(c==2){
					n=Integer.parseInt(s1)-Integer.parseInt(s2);
					tf.setText(String.valueOf(n));
				}
			else 
				
				//		MULTIPLICATION		...
				if(c==3){
					n=Integer.parseInt(s1)*Integer.parseInt(s2);
					tf.setText(String.valueOf(n));
				}
			
				
				//		DIVISION	...
				if(c==4){
					try{
						int p=Integer.parseInt(s2);
						if(p!=0){
							n=Integer.parseInt(s1)/Integer.parseInt(s2);
							tf.setText(String.valueOf(n));
						}
						else
							tf.setText("!!!  ..  Infinite");						
					}
					catch(Exception i){}					
				}
			else
				
				//		MODLOUS		...
				if(c==5){
					n=Integer.parseInt(s1)%Integer.parseInt(s2);
					tf.setText(String.valueOf(n));
				}
		}
		
		
		
		//		DELETE		INSERTED		VALUE	...
		
		if(e.getSource()==b18){
			tf.setText("");
		}
		
		
		//		RESET		CALCULATOR		TO		'0'	...
		
		if(e.getSource()==b19){
			c=0;
			tf.setText("");
		}		
		
		
		//		SWITCH		OFF		THE		CALCULATOR	...
		if(e.getSource()==b20){
			System.exit(0);
		}
		
	}
		
		
		
	public static void main(String args[]){
		mycalculator ob=new mycalculator();
	}	
	
	

}
