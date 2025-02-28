# 📝 Regular Expressions (Regex) Exercises  

Try to solve these regex challenges! Each exercise provides a **sample input** and the **expected output**. 

Tool: https://regex101.com/

---

## **Exercise 1: Extract Email Addresses**  
**Task:** Find and extract all valid email addresses from the given text.  

### Sample Input:
```
Contact us at support@example.com or sales@company.org for more info.  
You can also reach out to admin_123@web.net.
```

### Expected Output:
support@example.com  
sales@company.org  
admin_123@web.net  

---

## **Exercise 2: Extract MAC Addresses**  
**Task:** Identify and extract all MAC addresses from the text.  
*A MAC address follows the format `XX:XX:XX:XX:XX:XX` (hexadecimal values).*  

### Sample Input:
```
The network devices have the following MAC addresses: 00:1A:2B:3C:4D:5E,  
1B:22:33:AA:BB:CC, and FF:FF:FF:FF:FF:FF.  
```

### Expected Output:
00:1A:2B:3C:4D:5E  
1B:22:33:AA:BB:CC  
FF:FF:FF:FF:FF:FF  

---

## **Exercise 3: Validate IPv4 Addresses**  
**Task:** Extract all valid IPv4 addresses from the text.  
*An IPv4 address consists of four numbers (0-255) separated by dots.*  

### Sample Input:
```
The servers are hosted at 192.168.1.1, 10.0.0.255, and 256.100.50.25.  
```

### Expected Output:
192.168.1.1  
10.0.0.255  

---

## **Exercise 4: Extract Dates in `YYYY-MM-DD` Format**  
**Task:** Extract all dates written in the `YYYY-MM-DD` format from the text.  

### Sample Input:
```
Important dates: Project start - 2023-08-15, Deadline - 2024-01-30, Review - 2023/12/05.  
```

### Expected Output:
2023-08-15  
2024-01-30  

---

## **Exercise 5: Find Hashtags**  
**Task:** Extract all hashtags from a social media post.  
*A hashtag starts with `#` followed by letters, numbers, or underscores.*  

### Sample Input:
```
Loving the #CyberSecurity community! #Hacker #CTF_Challenge #regex123  
```

### Expected Output:
#CyberSecurity  
#Hacker  
#CTF_Challenge  
#regex123  

---

## **Exercise 6: Validate Strong Passwords**  
**Task:** Extract passwords that meet the following criteria:  
- At least **8 characters** long  
- Contains **at least one uppercase letter**  
- Contains **at least one lowercase letter**  
- Contains **at least one number**  
- Contains **at least one special character** (`!@#$%^&*`)  

### Sample Input:
```
Valid passwords: P@ssw0rd!, Secure#123, WrongPassword, hello123!
```

### Expected Output:
P@ssw0rd!  
Secure#123  

---

## **Exercise 7: Extract Phone Numbers**  
**Task:** Extract all phone numbers in the format `(XXX) XXX-XXXX`.  

### Sample Input:
```
Call us at (123) 456-7890 or (987) 654-3210.  
Another format like 123-456-7890 is invalid.  
```

### Expected Output:
(123) 456-7890  
(987) 654-3210  

---

## **Exercise 8: Extract URLs**  
**Task:** Extract all valid URLs from the text.  

### Sample Input:
```
Check out https://www.example.com, http://testsite.org, and our page at www.website.net.  
```

### Expected Output:
https://www.example.com  
http://testsite.org  
www.website.net  

---

## **Exercise 9: Extract HTML Tags**  
**Task:** Extract all HTML tags from the given text.  

### Sample Input:
```
The webpage contains <html>, <head>, <title>Sample</title>, and <body> elements.  
```

### Expected Output:
<html>  
<head>  
<title>  
</title>  
<body>  

---

## **Exercise 10: Find Duplicate Words**  
**Task:** Identify duplicate words appearing consecutively in a sentence.  

### Sample Input:
```
This is is a test test sentence with with duplicate words words.  
```

### Expected Output:
is is  
test test  
with with  
words words  

---

# ✅ Regular Expressions (Regex) Answers  

Here are the regex patterns that can be used to solve each exercise.  

---

## **Exercise 1: Extract Email Addresses**  
**Regex Pattern:**  
`[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}`  

`\w+\@\w+\.\w+`

---

## **Exercise 2: Extract MAC Addresses**  
**Regex Pattern:**  
`([0-9A-Fa-f]{2}:[0-9A-Fa-f]{2}:[0-9A-Fa-f]{2}:[0-9A-Fa-f]{2}:[0-9A-Fa-f]{2}:[0-9A-Fa-f]{2})`  

`[\w+]{2}:[\w+]{2}:[\w+]{2}:[\w+]{2}:[\w+]{2}:[\w+]{2}`

---

## **Exercise 3: Validate IPv4 Addresses**  
**Regex Pattern:**  
`\b((25[0-5]|2[0-4][0-9]|1[0-9][0-9]|[1-9]?[0-9])\.){3}(25[0-5]|2[0-4][0-9]|1[0-9][0-9]|[1-9]?[0-9])\b`  

`[\d+]{1,}\.[\d+]{1,}\.[\d+]{1,}\.[\d+]{1,}`

---

## **Exercise 4: Extract Dates in `YYYY-MM-DD` Format**  
**Regex Pattern:**  
`\b\d{4}-\d{2}-\d{2}\b`  

`[\d+]{4}[-\/][\d+]{2}[-\/][\d+]{2}`

---

## **Exercise 5: Find Hashtags**  
**Regex Pattern:**  
`#\w+`  

---

## **Exercise 6: Validate Strong Passwords**  
**Regex Pattern:**  
`^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[@$!%*?&#])[A-Za-z\d@$!%*?&#]{8,}$`  

`[a-zA-Z0-9!@#$%^&*]{8,}`

Hard

---

## **Exercise 7: Extract Phone Numbers**  
**Regex Pattern:**  
`\(\d{3}\) \d{3}-\d{4}`  

`\(?\d{3}\)?[\s-]\d{3}[\s-]\d{4}` - if capture all

---

## **Exercise 8: Extract URLs**  
**Regex Pattern:**  
`(https?:\/\/[^\s]+|www\.[^\s]+)`  

`(\w+:\/\/)*\w+\.\w+(\.\w+)*`

---

## **Exercise 9: Extract HTML Tags**  
**Regex Pattern:**  
`<[^>]+>`  

`<\/?\w+>`

---

## **Exercise 10: Find Duplicate Words**  
**Regex Pattern:**  
`\b(\w+)\s+\1\b`  


