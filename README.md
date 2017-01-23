import java.util.*;
import java.awt.*;
public class SierpinskiCarpet {
	public static final int SIZE = 729;
    public static final DrawingPanel panel = new DrawingPanel(SIZE,SIZE);
    public static void main(String[] args) {
        int max =3;
        int num= 0;
        int s = SIZE;
        for (int i =0; i<max; i++){
        	s = s/3;
        }
    
        int x =s;
        int y=s;
        square( s, max, x , y);
        int red = (int) (Math.random() * 255);
        int green = (int) (Math.random() * 255);
        int blue = (int) (Math.random() * 255);
    } 
    public static void square( int s, int max, int x, int y){
        Graphics g = panel.getGraphics();
        
      
   
        if( max>1){
        	g.fillRect( s, s, s, s);
        	g.fillRect( s+3*s, s, s, s);
        	g.fillRect( s+3*s, s+3*s, s, s);
        	g.fillRect( s+3*s, s+2*3*s, s, s);
        	g.fillRect( s, s+3*s, s, s);
        	g.fillRect( s+3*s, s+3*s, s, s);
        	 square(s*3, max-1, x,y);
        	 
        }
        else
        	g.fillRect( SIZE/3, SIZE/3, s, s);
      
        /*	g.fillRect(x +s, y, s/3,s/3);
        	
        	g.fillRect(x, y+2*(s) ,s/3,s/3);
        	g.fillRect( x+2*(s), y, s/3,s/3);
        	g.fillRect(x+(s), y+(s), s/3,s/3);
        	g.fillRect(x+2*(s), y+2*(s), s/3,s/3);
        	g.fillRect(x+2*(s), y+(s), s/3,s/3);
        	g.fillRect(x+(s), y+2*(s),s/3,s/3);
        	g.fillRect(x,y+(s),s,s/3/3); */
    }
        	
}
