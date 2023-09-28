# Java-interview-cheat-sheet

### Code Samples
Twosum:
```
class Solution {
    public int[] twoSum(int[] nums, int target) {
        HashMap<Integer, Integer> mp = new HashMap<Integer, Integer>();
        int[] res;
        for (int i = 0; i < nums.length; i++){
            int complement = target - nums[i];
            if (mp.containsKey(nums[i])){
                return new int[] {i, mp.get(nums[i])};
            } else {
                mp.put(complement, i);
            }
        }
        return new int[] {};
    }
}
```
### Java language semantics: 
- A public variable is accessible from anywhere (well, anywhere where the class is accessible). A private variable is only accessible inside the class. **A static variable belongs to the class rather than to an instance of a class.**
- Java int vs. Integer type: an int simply represents a whole number, while an Integer has additional properties and methods. The int is one of Java’s eight Java *primitive* types, while the Integer wrapper class is one of hundreds of components included in the Java API. For example, if you want to declare a hash map of integer key-value pairs, `HashMap<Integer, Integer> mp = new HashMap<Integer, Integer>();`
- Take note of the `new` keyword to create a new HashMap, Set, ArrayList, etc.!
- `System.out.println("hi");`
  
### Set
Set interface is declared as `public interface Set extends Collection`
`Set<Integer> s = new Set<Integer>();`
List of common methods:
- s.add(elem);
- s.remove(elem);
- s.isEmpty();
- s.size();
- s.toArray()
- s.clear()

There's also SortedSet, TreeSet, EnumSet, HashSet, 

### Arraylist
```
import java.util.ArrayList
ArrayList<String> cars = new ArrayList<String>("BMW, Toyota");
cars.add("Jeep"); // add to list
cars.add("tank");
cars.get(1); // access list
cars.set(0, "Honda"); // change item in list
cars.remove(0); // remove elem at idx 0 in arraylist
cars.size()
```

### Java string
```
String s = "fasd"
s.charAt(index)
s.toLowerCase()
s.toUpperCase()
s.isLetterOrDigit()
// If you would like to use these methods per Character in the string, use the Character class
Character.isLetterOrDigit(s.charAt(index))
Character.toLowerCase(s.charAt(index))
```
Syntactically, "pointers" don't really exist in Java. 

