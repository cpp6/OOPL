import java.util.*;

class Product {

	String name;
	double price;
	int quantity;

	Product() {
		this.name = "Default";
		this.price = 0.0;
		this.quantity = 0;
	}

	Product(String name, double price) {
		this.name = name;
		this.price = price;
		this.quantity = 1;
	}

	Product(String name, double price, int quantity) {
		this.name = name;
		this.price = price;
		this.quantity = quantity;
	}

	double getTotal() {
		return price * quantity;
	}

	// Function for applying discount
	static double applyDiscount(double total) {
		if (total > 500) {
            return total * 0.85; // 15% discount
        } else if (total > 200) {
            return total * 0.90; // 10% discount
        } else if (total > 100) {
            return total * 0.95; // 5% discount
        }
        return total;
	}
}

public class Ecommerce {

	public static void main(String args[]) {
		Scanner sc = new Scanner(System.in);

		Product p1 = new Product("Laptop", 50, 1);
		Product p2 = new Product("Phone", 20, 1);

		System.out.println("Enter name of product: ");
		String name = sc.nextLine();

		System.out.println("Enter price: ");
		double price = sc.nextDouble();

		System.out.println("Enter quantity: ");
		int quantity = sc.nextInt();

		Product userProduct = new Product(name, price, quantity);

		double total = p1.getTotal() + p2.getTotal() + userProduct.getTotal();
		double finalAmount = Product.applyDiscount(total);
		double discount = total - finalAmount;
		
		System.out.println("------------------------- invoice --------------------------");
		System.out.println("name\t\tQty\t\tPrice\t\tTotal");
		System.out.println(p1.name + "\t\t" + p1.quantity + "\t\t" + p1.price + "\t\t" + p1.getTotal());
		System.out.println(p2.name + "\t\t" + p2.quantity + "\t\t" + p2.price + "\t\t" + p2.getTotal());
		System.out.println(userProduct.name + "\t\t" + userProduct.quantity + "\t\t" + userProduct.price + "\t\t" + userProduct.getTotal());
		System.out.println("------------------------------------------------------------");
		System.out.println("Total: " + total);
		System.out.println("Discount: " + discount);
		System.out.println("Final Amount: " + finalAmount);

		sc.close();
	}
}
