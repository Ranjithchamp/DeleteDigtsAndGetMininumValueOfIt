# DeleteDigtsAndGetMininumValueOfIt

import java.util.Arrays;
import java.util.Scanner;

public class DeletingDigits {

	public static void main(String[] args) {

		Scanner get = new Scanner(System.in);
		System.out.println("Enter the number");
		int d = get.nextInt();
		int digit = d;
		int count = 0;
		while (digit != 0) {
			++count;
			digit = digit / 10;
		}
		int l;
		int i = 0;
		int array[] = new int[count];
		while (d != 0) {
			array[i++] = d % 10;
			d = d / 10;
		}
		int output = 0;
		Arrays.sort(array);
		System.out.println("enter no. of digit to be deleted");
		int b=get.nextInt();
		for (int j = 0; j < array.length - b; j++) {
			output = output * 10;
			output = output + array[j];
		}
System.out.println("After deleting three Digits minimun posilbe number is:");
		System.out.println(output);
	}

}
