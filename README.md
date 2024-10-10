# PrintFirstNonRepeatCharacter

Problem Statement:
Find the First Non-Repeating Character
Write a program to find the first non-repeating character in a string. For input "swiss", the output
should be "w". You cannot use any built-in string or character frequency counting functions.
Instructions: Implement manual string traversal and counting logic to solve the problem.

CODE:

import java.util.Scanner;
public class FirstNonRepeat {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in); 
        System.out.println("Enter the string: ");
        String input = sc.nextLine(); 
        boolean found = false; 
        for (int i = 0; i < input.length(); i++) {
            boolean unique = true; 
            for (int j = 0; j < input.length(); j++) {
                if (i != j && input.charAt(i) == input.charAt(j)) {
                    unique = false;  
                    break; 
                }
            }
            if (unique) { 
                System.out.println("First non-repeating character: " + input.charAt(i));
                found = true;
                break;  
            }
        }
        if (!found) {  
            System.out.println("No non-repeating character found.");
        }
        sc.close();
    }
}

Sample Inputs and Outputs:
1. Input: swiss
   
Output: w

3. Input: aabbcc

Output: No non-repeating character found.

4. Input: alphabet

Output: l
