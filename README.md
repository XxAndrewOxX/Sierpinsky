# Sierpinsky
public class SierpinksiOpio {
	public static final int SIZE = 729;
	public static DrawingPanel panel = new DrawingPanel(SIZE, SIZE);
	
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int num= 3;
		square(num);

	} 
	public static void square(int num){
		Graphics g = panel.getGraphics();
		if( num>0){
		g.fillRect(SIZE/(3*num), SIZE/(3*num), (SIZE/3), (SIZE/3));
		
		square(num-1);
		}
	}


}
