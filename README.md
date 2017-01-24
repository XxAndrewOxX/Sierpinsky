	import java.util.*;
import java.awt.*;
public class SierpinskiCarpet {
	
		public static final int SIZE = 729;
		public static final DrawingPanel panel = new DrawingPanel(SIZE,SIZE);
		
		public static void main(String[] args) {
			// TODO Auto-generated method stub
			int max =9;
			int num= 0;
			//int s = (int) ((SIZE)/ (Math.pow(3, max)));
			square(SIZE, max, SIZE, SIZE);
			int red = (int) (Math.random() * 255);
	        int green = (int) (Math.random() * 255);
	        int blue = (int) (Math.random() * 255);

		} 
		
		 
		public static void square( int s, int max, int x, int y){
		    Graphics g = panel.getGraphics();
		    Random rand= new Random();
			Color color = new Color(rand.nextInt(256), rand.nextInt(256), rand.nextInt(256), rand.nextInt(256));

			g.setColor(color);
		    if(s>0){
		    
		    g.fillRect(x/3, y/3, s/3, s/3);
		    square(  max, s/3, x+(s*4)/3,  y- 2*s/3);
		    square( max, s/3, x-(s*2)/3,  y- 2*s/3);
		    square( max, s/3, x+s/3, y+ (s*4)/3);
			square(  max, s/3, x+(s*4)/3, y+(s*4)/3);
			square( max, s/3, x-(s*2)/3, y+(s*4)/3);
			square( max, s/3, x+(s*4)/3, y+s/3);
			square(  max, s/3, x-(s*2)/3, y+ s/3);
			square( max, s/3, x+s/3, y- 2*s/3);
		    }
		   
		}
		}
