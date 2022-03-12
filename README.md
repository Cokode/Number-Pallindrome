# Number-Pallindrome
This projects check if given number is a Palindrome number and returns true and false if otherwise


public class NumberPalindrome {

    public static void main(String[] args) {
        System.out.println(isPalindrome(-1221));
    }

    public static boolean isPalindrome(int number) {
        if(number <= 10 && number > 0 ) {
            return false;
        }
        int reverse = 0;
        int result = 0;
        result += number;

        while (number != 0) {
            int lastDigit = number % 10;
            reverse *= 10;
            reverse += lastDigit;
            number /= 10;
        }
        return reverse == result;
    }

}
