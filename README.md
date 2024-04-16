import java.util.Scanner;

public class CustomerServiceChatSystem {
    
    public void start() {
        Scanner scanner = new Scanner(System.in);
        
        System.out.println("Welcome to Customer Service Chat System!");
        System.out.println("How can we assist you today?");
        
        while (true) {
            System.out.print("You: ");
            String userMessage = scanner.nextLine();
            
            if (userMessage.equalsIgnoreCase("exit")) {
                System.out.println("Thank you for using our Customer Service Chat System. Goodbye!");
                break;
            }
            
            String response = generateResponse(userMessage);
            System.out.println("Customer Service: " + response);
        }
        
        scanner.close();
    }
    
    private String generateResponse(String message) {
        return "Thank you for reaching out. We will get back to you shortly.";
    }
    
    public static void main(String[] args) {
        CustomerServiceChatSystem chatSystem = new CustomerServiceChatSystem();
        chatSystem.start();
    }
}
