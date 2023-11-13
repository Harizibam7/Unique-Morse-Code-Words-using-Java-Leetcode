# Unique-Morse-Code-Words-using-Java-Leetcode

    class Solution {
        public int uniqueMorseRepresentations(String[] words) {
            String b[]={".-","-...","-.-.","-..",".","..-.","--.","....","..",".---","-.-",".-..","--","-.","---",".--.","--.-",".-.","...","-","..-","...-",".--","-..-","-.--","--.."};
            Set<String> set = new HashSet<String>(); 
            for(String word : words){
                String demo = "";
                for(int i =0;i<word.length();i++){
                    demo +=b[word.charAt(i)-97];   
                }
                set.add(demo);
            }
            return set.size();
        }
    }
