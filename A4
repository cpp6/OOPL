import java.util.*;

public class HotelBooking{
	public static void main(String args[]){
		Scanner sc = new Scanner(System.in);
		int floor = 3;
		int roomsperfloor = 5;
		int[][] rooms = new int[floor][roomsperfloor];

		while(true){
			System.out.println("===Hotel Menu===");
			System.out.println("1. View Rooms");
			System.out.println("2. Book room");
			System.out.println("3. Checkout");
			System.out.println("4. Exit");

			
			System.out.println("Enter choice: ");
			int choice = sc.nextInt();

			switch(choice){

			case 1:
				System.out.println("Rooms status: (0->Available, 1->Booked)");
				for(int i = 0; i< floor; i++){
					System.out.print("Floor: "+(i+1)+": ");
					for(int j = 0; j < roomsperfloor; j++){
						System.out.print(rooms[i][j]+" ");
					}
					System.out.println();
				}
			break;
			
			case 2:
				System.out.println("Enter floor number: ");
				int f = sc.nextInt();

				System.out.println("Enter room number: ");
				int r = sc.nextInt();

				int fi = f - 1;
				int ri = r - 1;

				if(fi>=0 && fi<floor && ri>=0 && ri<roomsperfloor){
					
					if(rooms[fi][ri]==0){
						rooms[fi][ri]=1;
							
					System.out.println("Room booked successfully!");
					}else{
						System.out.println("Room is not available");
					}

				}else{
					System.out.println("Invalid room or floor number!");
				}
			break;

			case 3:
				System.out.println("Enter floor number(1-3): ");
				int cf = sc.nextInt();

				System.out.println("Enter room number(1-5): ");
				int cr = sc.nextInt();

				int cfi = cf - 1;
				int cri = cr - 1;
				
				if(cfi>=0 && cfi < floor&&cri >= 0 && cri < roomsperfloor){
					if(rooms[cfi][cri]==1){
						rooms[cfi][cri]=0;
						System.out.println("Successfully checkout from room!");
					}else{
						System.out.println("Room already available or checkout!");
					}
				}else{
					System.out.println("Invalid room or floor number!");
				}
			break;

			case 4:
				System.out.println("Thankuu!");
				sc.close();
				return;
				

			default:
				System.out.println("Invalid choice!!!");
			
			}	
		}
	}
}
