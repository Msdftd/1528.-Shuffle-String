# 1528.-Shuffle-String
1528. Shuffle String leetcode Solution

public class ShuffleString {
    public static String restoreString(String s, int[] indices) {
        char[] shuffled = new char[s.length()];
        
        for (int i = 0; i < s.length(); i++) {
            shuffled[indices[i]] = s.charAt(i);
        }
        
        return new String(shuffled);
    }
    
    public static void main(String[] args) {
        String s = "codeleet";
        int[] indices = {4, 5, 6, 7, 0, 2, 1, 3};
        String shuffled = restoreString(s, indices);
        System.out.println("Input String: " + s);
        System.out.println("Shuffled String: " + shuffled);
    }
}
