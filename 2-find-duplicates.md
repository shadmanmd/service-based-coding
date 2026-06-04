# Find Duplicates
Input: [10, 20, 10, 30, 40, 30]
Output: [10, 30]

```python
# python
def find_duplicates(arr):
    seen = set()
    duplicates = set()
    for num in arr:
        if num in seen:
            duplicates.add(num)
        seen.add(num)
    return list(duplicates)

print(find_duplicates([10, 20, 10, 30, 40, 30]))  # [10, 30]
```

```javascript
// javascript 
function findDuplicates(arr) {
    const seen = new Set();
    const duplicates = new Set();
    for (const num of arr) {
        if (seen.has(num)) duplicates.add(num);
        seen.add(num);
    }
    return [...duplicates];
}

console.log(findDuplicates([10, 20, 10, 30, 40, 30])); // [10, 30]
```

```java
// java
import java.util.*;

public class FindDuplicates {
    public static List<Integer> findDuplicates(int[] arr) {
        Set<Integer> seen = new HashSet<>();
        Set<Integer> duplicates = new LinkedHashSet<>(); // preserves insertion order
        
        for (int num : arr) {
            if (seen.contains(num)) duplicates.add(num);
            seen.add(num);
        }
        
        return new ArrayList<>(duplicates);
    }

    public static void main(String[] args) {
        int[] arr = {10, 20, 10, 30, 40, 30};
        System.out.println(findDuplicates(arr)); // [10, 30]
    }
}
```
