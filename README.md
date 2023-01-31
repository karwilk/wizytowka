import java.util.Scanner;

public class BusinessCardMS {

    public static void main(String[] args) {
        // TODO Auto-generated method stub
        Scanner scanner = new Scanner(System.in);

        System.out.print("Podaj imię: ");
        String name = scanner.next();
        System.out.print("Podaj nazwisko: ");
        String surname = scanner.next();

        System.out.print("Podaj numer telefonu: ");
        int phone = scanner.nextInt();
        System.out.print("Podaj miasto lub miejscowość: ");
        String city = scanner.next();

        String line1 = "* " + name + " " + surname;
        String line2 = "* tel. " + phone + " adres: " + city;

        int line1Length = line1.length();
        int line2Length = line2.length();

        int longerLineLength;

        // wyznacznie najdłużej linii
        if(line1Length > line2Length) {
            longerLineLength = line1Length;
        } else {
            longerLineLength = line2Length;
        }


        String stars = "*".repeat(longerLineLength+2);

        System.out.println(stars);

        int roznica = 0;
        if (line1Length > line2Length) {
            roznica = line1Length - line2Length;
        } else {
            roznica = line2Length - line1Length;
        }

        String spacje = " ".repeat(roznica);

        if(line1Length == longerLineLength) {
            System.out.println(line1+ " *");
            System.out.println(line2+ spacje + " *");
        } else {
            System.out.println(line1+ spacje + " *");
            System.out.println(line2+" *");
        }

        System.out.println(stars);


    }

}
