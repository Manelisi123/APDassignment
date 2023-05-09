# Group Members
# Manelisi Khoza 220211523
# Boniface Ramushu 202090213
# Rejoice Ngobeni 219072868
# Nomfundo Buda 202000354
# Thobejane Tshegofatso 219060746


# AVPD assignment
This Java program prompts the user for two integers, compares them, and outputs the larger value. The code was missing necessary JUnit testing imports and contained a typo in the Scanner object initialization. We fixed these issues and included a JUnit test class to ensure program functionality.

import org.junit.Assert;
import org.junit.Test;
import org.junit.runner.RunWith;
import org.junit.runners.JUnit4;
import java.util.Scanner;

@RunWith(JUnit4.class)
public class largerinteger2Test {

    @Test
    public void testLargerInteger() {
        Scanner scanner = new Scanner("5\n10\n");
        int firstInt = scanner.nextInt();
        int secondInt = scanner.nextInt();
        int expected = 10;
        int actual = 0;
        if (firstInt > secondInt) {
            actual = firstInt;
        } else {
            actual = secondInt;
        }
        Assert.assertEquals(expected, actual);
    }
}

public class largerinteger2 {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Enter the first integer: ");
        int firstInt = scanner.nextInt();
        System.out.println("Enter the second integer: ");
        int secondInt = scanner.nextInt();
        if (firstInt > secondInt) {
            System.out.println("The larger integer is: " + firstInt);
        } else {
            System.out.println("The larger integer is: " + secondInt);
        }
    }
}
