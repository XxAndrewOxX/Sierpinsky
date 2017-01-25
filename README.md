import java.awt.*;
import java.util.*;
public class SiepinksyCarpet2 {
	public static final int SIZE = 729;
	public static final DrawingPanel panel = new DrawingPanel(SIZE,SIZE);

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		//panel.setBackground(Color.BLACK);
		Graphics g = panel.getGraphics();
		int size = SIZE;
		Square( size, size, size);
	}
	public static void Square(  int size, int x, int y){
		Random rand= new Random();
		Graphics g = panel.getGraphics();
		Color color = new Color(rand.nextInt(256), rand.nextInt(256), rand.nextInt(256), rand.nextInt(256));
		if(size>0){
		g.setColor(color);
		//panel.sleep(1);
		g.fillRect(x/3, y/3, size/3, size/3);
		
		Square( size/3, x+size/3, y+ (size*4)/3);
		Square( size/3, x+(size*4)/3, y+(size*4)/3);
		Square(  size/3, x-(size*2)/3, y+(size*4)/3);
		Square( size/3, x+(size*4)/3, y+size/3);
		Square(  size/3, x-(size*2)/3, y+ size/3);
		Square(  size/3, x+(size*4)/3,  y- 2*size/3);
		Square(  size/3, x-(size*2)/3,  y- 2*size/3);
		Square(  size/3, x+size/3, y- 2*size/3);
		}
	}

}
