import java.util.ArrayList;
import java.util.List;

class Product {
    String name;
    double price;
    double discount;

    public Product(String name, double price, double discount) {
        this.name = name;
        this.price = price;
        this.discount = discount;
    }
}

public class ShoppingCart {
    List<Product> items = new ArrayList<>();

    public void addProduct(Product product) {
        items.add(product);
    }

    public double calculateSubtotal() {
        double subtotal = 0;
        for (Product item : items) {
            subtotal += item.price;
        }
        return subtotal;
    }

    public double calculateSavings() {
        double savings = 0;
        for (Product item : items) {
            savings += item.price * item.discount;
        }
        return savings;
    }

    public double calculateFinalTotal() {
        double subtotal = calculateSubtotal();
        double savings = calculateSavings();
        return subtotal - savings;
    }

    public void printBill() {
        System.out.println("**** Bill ****");
        for (Product item : items) {
            System.out.println(item.name + ": $" + item.price);
        }
        System.out.println("Subtotal: $" + calculateSubtotal());
        System.out.println("Savings: $" + calculateSavings());
        System.out.println("Final Total: $" + calculateFinalTotal());
        System.out.println("*********");
    }

    public static void main(String[] args) {
        Product product1 = new Product("Product 1", 10.0, 0.1);
        Product product2 = new Product("Product 2", 20.0, 0.15);
        Product product3 = new Product("Product 3", 15.0, 0.2);
        Product product4 = new Product("Product 4", 12.0, 0.1);
        Product product5 = new Product("Product 5", 25.0, 0.25);

        ShoppingCart cart = new ShoppingCart();
        cart.addProduct(product1);
        cart.addProduct(product2);
        cart.addProduct(product3);
        cart.addProduct(product4);
        cart.addProduct(product5);

        cart.printBill();
    }
}
