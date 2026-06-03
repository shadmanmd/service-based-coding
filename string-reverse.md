# 1. Reverse a string
Approach 1:
Reverse for loop
```java
// java
String str = "hello";
String res = "";
for(int i = str.length()-1; i>=0; i--) {
    res += str.charAt(i);
}
System.out.println(res);
```

```javascript
// javascript
let str = "hello";
let res = "";
for(let i = str.length-1; i>=0; i--) {
    res += str[i];
}
console.log(res);
```

```python
# python method 1
s = "hello"
res = ""
for i in range(len(s)-1, -1, -1):
    res += s[i]
print(res)
```

```python
# python method 2
s = "hello"
print(s[::-1])
```

Approach 2:
Using while loop and two pointers
```java
// java
String str = "hello";
char[] arr = str.toCharArray();
int i = 0, j = arr.length - 1;
while (i < j) {
    char temp = arr[i];
    arr[i] = arr[j];
    arr[j] = temp;
    i++;
    j--;
}
str = new String(arr);
System.out.println(str);
```

```javascript
// javasacript
let str = "hello";
let arr = str.split('');
let i = 0, j = arr.length - 1;
while (i < j) {
    let temp = arr[i];
    arr[i] = arr[j];
    arr[j] = temp;
    i++;
    j--;
}
str = arr.join('');
console.log(str);
```
```python
# python
s = "hello"
arr = list(s)
i = 0
j = len(arr) - 1
while i < j:
    arr[i], arr[j] = arr[j], arr[i]
    i += 1
    j -= 1
s = "".join(arr)
print(s)
```
