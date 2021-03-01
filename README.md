# Chapter-1-Lab-5a

Lab Goal :   This lab was designed to teach you more object oriented programming and how to write a very simple game, using interfaces, abstract classes, and inheritance.

Lab Description :   Complete the code for the abstract class Drawable located in Drawable.java.  Drawable will be extended to make a Piece class.  Piece will store name and location information for a game piece that could be used in a board game.  Use PieceTester.java to test the completed Piece class.

Files Needed ::
Locatable.java
Drawable.java
Nameable.java
Piece.java
Main.java

public interface Locatable
{

  public void setPos( int x, int y);
  public void setX( int x );
  public void setY( int y );
	
  public int getX();
  public int getY();
}


public abstract class Drawable implements Locatable
{
   private int xPos;
   private int yPos;
   private int width;
   private int height;


   //constructors


   //set methods

	
   //get methods

	
   public abstract void draw(Graphics window);

	
   //toString
}


public interface Nameable
{
   public void setName(String n);
   public String getName();
}


public class Piece extends Drawable implements Nameable
{
   private String name;
   private Color color;
	
   //constructors


   //sets and gets

	
   public void draw(Graphics window)
   {
	window.setFont(new Font("TAHOMA",Font.BOLD,28));
	window.setColor(getColor());
	window.drawRect(getX(),getY(),getWidth(),getHeight());
	window.drawString(getName(),getX()+10,getY()+30);
   }
	
   //toString
}

Sample Output ( PieceTester.java )

5 5 5 5 empty java.awt.Color[r=0,g=0,b=255]
5 5 5 5 red checker java.awt.Color[r=0,g=0,b=255]
100 100 5 5 the shoe from a money game java.awt.Color[r=0,g=0,b=255]
200 200 20 20 bishop java.awt.Color[r=255,g=255,b=255]
