
# ------------------------------1st--------------------------------------

# Find second highest values in array without using predefined functions.

public class SecondHighestValue {
    public static void main(String[] args) {
        int[] arr = {12, 35, 1, 10, 34, 1}; 
        int secondHighest = findSecondHighest(arr);

        System.out.println(secondHighest);
        
    }

    public static int findSecondHighest(int[] arr) {
        if (arr.length < 2) {
            return Integer.MIN_VALUE;  
        }

        int highest = Integer.MIN_VALUE;
        int secondHighest = Integer.MIN_VALUE;

        for (int i = 0; i < arr.length; i++) {
            if (arr[i] > highest) {
                secondHighest = highest;
                highest = arr[i];
            } else if (arr[i] > secondHighest && arr[i] < highest) {
                secondHighest = arr[i];
            }
        }

        return secondHighest;
    }
}


# -----------------2nd-------------------------------

# Find product of given 2 A,B matrices 2 X 2, Product matrix C. Print C matrix elements
# 2 3        2 4         10 11
# 1 2        2 1         6    6


public class MatrixMultiplication {
    public static void main(String[] args) {
        int[][] A = {
            {2, 3},
            {1, 2}
        };

        int[][] B = {
            {2, 4},
            {2, 1}
        };

        int[][] C = new int[2][2];

        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 2; j++) {
                C[i][j] = 0;
                for (int k = 0; k < 2; k++) {
                    C[i][j] += A[i][k] * B[k][j];
                }
            }
        }

        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 2; j++) {
                System.out.print(C[i][j] + " ");
            }
            System.out.println();
        }
    }
}


# --------------------------3rd--------------------------------------------

# Find repeated element with high frequency an array , print it.
# [ 3,4,5,2,3,4,6,7,8,5,3,6,7,8,3] ans=3


import java.util.HashMap;

public class MostFrequentElement {
    public static void main(String[] args) {
        int[] arr = {3, 4, 5, 2, 3, 4, 6, 7, 8, 5, 3, 6, 7, 8, 3};
        int mostFrequentElement = findMostFrequentElement(arr);

        System.out.println(mostFrequentElement);
    }

    public static int findMostFrequentElement(int[] arr) {
        HashMap<Integer, Integer> elementCount = new HashMap<>();
        int maxCount = 0;
        int mostFrequentElement = arr[0];

        for (int num : arr) {
            int count = elementCount.getOrDefault(num, 0) + 1;
            elementCount.put(num, count);

            if (count > maxCount) {
                maxCount = count;
                mostFrequentElement = num;
            }
        }

        return mostFrequentElement;
    }
}


# --------------------------4th--------------------------------------------

#  Find first last repeating character in a given string.
# Input : language
# Output :g


import java.util.HashMap;

public class LastRepeatingChar {
    public static void main(String[] args) {
        String s = "language";
        char lastRepeating = '\0'; 
        HashMap<Character, Integer> charCount = new HashMap<>();

        for (int i = 0; i < s.length(); i++) {
            char currentChar = s.charAt(i);
            charCount.put(currentChar, charCount.getOrDefault(currentChar, 0) + 1);
        }

        for (int i = s.length() - 1; i >= 0; i--) {
            if (charCount.get(s.charAt(i)) > 1) {
                lastRepeating = s.charAt(i);
                break;
            }
        }

        System.out.println( lastRepeating);

    }
}



# --------------------------5th--------------------------------------------

# Reverse words in a given string without using predefined functions.
# Input:  i love programming very much
# Output   : much very programming love i


public class ReverseWords {
    public static void main(String[] args) {
        String s = "i love programming very much";
        String reversedString = "";
        int length = s.length();
        int wordEnd = length;

 
        for (int i = length - 1; i >= 0; i--) {
            if (s.charAt(i) == ' ' || i == 0) {
                int wordStart;
                if (i == 0) {
                    wordStart = 0;
                } else {
                    wordStart = i + 1;
                }

            
                for (int j = wordStart; j < wordEnd; j++) {
                    reversedString += s.charAt(j);
                }

                if (i > 0) {
                    reversedString += ' ';
                }

                wordEnd = i;
            }
        }

     
        System.out.println(reversedString);
    }
}


# --------------------------6th--------------------------------------------

# Find count of distinct subsequences in a string.
# Input “var” v a r
# The seven distinct subsequences are “”, “v”, “a”, “r”, “va”, “av” ,”ar”,”ra”,”vr”,”rv”,”var”,”rva”,”rav”,”avr”,”arv”,….


