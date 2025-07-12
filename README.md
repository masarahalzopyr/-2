# -2
   public class Circle extends Shape {
    private double radius=1.0;
    public Circle(String color, boolean filled, double radius) {
        super(color, filled);
        this.radius = radius;
    }
    public double getRadius() {
        return radius;
    }
    public void setRadius(double radius) {
        this.radius = radius;
    }
    @Override
    public double getArea() {
        return Math.PI * radius * radius;
    }
    @Override
    public double getPerimeter() {
        return 2 * Math.PI * radius;
    }
}
public class Rectangle extends Shape {
    private double width = 1.0;
    private double length = 1.0;

   public Rectangle() {     
    }
    public Rectangle(double width, double length) {
        this.width = width;
        this.length = length;
    }
    public Rectangle(double width, double length, String color, boolean filled) {
        super(color, filled); // استدعاء constructor الأب مع باراميترات
        this.width = width;
        this.length = length;
    }
    public double getWidth() {
        return width;
    }
    public void setWidth(double width) {
        this.width = width;
    }
    public double getLength() {
        return length;
    }
    public void setLength(double length) {
        this.length = length;
    }
    @Override
    public double getArea() {
        return width * length;
    }
    @Override
    public double getPerimeter() {
        return 2 * (width + length);
    }
    @Override
    public String toString() {
        return "Rectangle[" + super.toString() + ", width=" + width + ", length=" + length + "]";
    }
}
    public class Square extends Rectangle {
    public Square() {}
    public Square(double side) {
        super(side, side);
    }
    public Square(double side, String color, boolean filled) {
        super(side, side, color, filled);
    }
    public double getSide() {
        return getWidth(); // أو getLength() نفس الشي
    }
    public void setSide(double side) {
        setWidth(side);
        setLength(side);
    }
    @Override
    public void setWidth(double side) {
        super.setWidth(side);
        super.setLength(side);
    }
    @Override
    public void setLength(double side) {
        super.setLength(side);
        super.setWidth(side);
    }
    @Override
    public String toString() {
        return "Square[" + super.toString() + "]";
    }

    
