import java.util.*;
import java.awt.*;
public class SierpinskiCarpet {
	
		public static final int SIZE = 729;
		public static final DrawingPanel panel = new DrawingPanel(SIZE,SIZE);
		
		public static void main(String[] args) {
			// TODO Auto-generated method stub
			int max =3;
			int num= 0;
			square(num, SIZE/3, max);
			int red = (int) (Math.random() * 255);
	        int green = (int) (Math.random() * 255);
	        int blue = (int) (Math.random() * 255);

		} 
		public static void square(int num, int s, int max ){
			Graphics g = panel.getGraphics();
			g.fillRect( s, s,s, s);
			if( num<max){
				g.fillRect( s+s/3, s,s/3, s/3);
				g.fillRect( s, s+s/3,s/3, s/3);
				g.fillRect( s, s+2*(s/3),s/3, s/3);
				g.fillRect( s+2*(s/3), s,s/3, s/3);
				g.fillRect( s+s/3, s+s/3,s/3, s/3);
				g.fillRect( s+2*(s/3), s+ 2*(s/3) ,s/3, s/3);
	
			square(num+1, s/3, max);
			}
		}
}
