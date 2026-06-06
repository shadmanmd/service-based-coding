# Leetcode classic two sum problem

```java
// java
import java.util.HashMap;
import java.util.Map;

public class Solution {
    public int[] twoSum(int[] nums, int target) {
        // Create a hash map to store the value and its corresponding index
        Map<Integer, Integer> numMap = new HashMap<>();
        
        // Iterate through the array
        for (int i = 0; i < nums.length; i++) {
            int complement = target - nums[i];
            
            // If the complement exists in the map, we found the pair
            if (numMap.containsKey(complement)) {
                return new int[] { numMap.get(complement), i };
            }
            
            // Otherwise, store the current number and its index in the map
            numMap.put(nums[i], i);
        }
        
        // Return an empty array if no solution is found (though the problem guarantees one)
        return new int[] {};
    }
}

```javascript
var twoSum = function(nums, target) {
    // Create a map to store the value and its corresponding index
    const numMap = new Map();
    
    // Iterate through the array
    for (let i = 0; i < nums.length; i++) {
        const complement = target - nums[i];
        
        // If the complement exists in the map, we found the pair
        if (numMap.has(complement)) {
            return [numMap.get(complement), i];
        }
        
        // Otherwise, store the current number and its index in the map
        numMap.set(nums[i], i);
    }
    
    // Return an empty array if no solution is found
    return [];
};

```
