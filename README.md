# MiNave
Videojuego de los años 80
import java.awt.Image;
import java.awt.event.KeyEvent;
import javax.swing.ImageIcon;

public class Avion {

    private int dx;
    private int dy;
    private int x;
    private int y;
    private Image image;

    public Avion() {
        
        initCraft();
    }
    
    private void initCraft() {
      Image ii = new ImageIcon(getClass().getResource("virus.png")).getImage();
    //    ImageIcon ii = new ImageIcon("craft.png");
        image = ii;
        x = 40;
        y = 60;        
    }


    public void move() {
        x += dx;
        y += dy;
    }

    public int getX() {
        return x;
    }

    public int getY() {
        return y;
    }

    public Image getImage() {
        return image;
    }

    public void keyPressed(KeyEvent e) {
      
        int key = e.getKeyCode();
          System.out.println(""+key);

        if (key == KeyEvent.VK_LEFT) {
            dx = -1;
        }

        if (key == KeyEvent.VK_RIGHT) {
            dx = 1;
        }

        if (key == KeyEvent.VK_UP) {
            dy = -1;
        }

        if (key == KeyEvent.VK_DOWN) {
            dy = 1;
        }
    }

    public void keyReleased(KeyEvent e) {
        System.out.println("");
        int key = e.getKeyCode();

        if (key == KeyEvent.VK_LEFT) {
            dx = 0;
        }

        if (key == KeyEvent.VK_RIGHT) {
            dx = 0;
        }

        if (key == KeyEvent.VK_UP) {
            dy = 0;
        }

        if (key == KeyEvent.VK_DOWN) {
            dy = 0;
        }
    }
}
