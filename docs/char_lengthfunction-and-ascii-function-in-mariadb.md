# Mariadb 中的 Char_Length()函数和 ASCII()函数

> 原文:[https://www . geesforgeks . org/char _ length function-and-ascii-function-in-mariadb/](https://www.geeksforgeeks.org/char_lengthfunction-and-ascii-function-in-mariadb/)

**1。CHAR_LENGTH()函数:**
在马里亚数据库中，用于计算字符串总字符长度的 CHAR_LENGTH 函数。在这个函数中，一个字符串将作为参数传递，它将返回该字符串的长度，它将是一个数字类型。

**语法:**

```
CHAR_LENGTH(string)
```

**参数:**必选。
**字符串:**它将返回字符串长度。

**示例-1 :**

```
SELECT CHAR_LENGTH('GEEKSFORGEEKS');
```

**输出:**

```
13
```

**例-2 :**

```
SELECT CHAR_LENGTH(' ');
```

**输出:**

```
1
```

**例-3 :**

```
SELECT CHAR_LENGTH('');
```

**输出:**

```
0
```

**例-4 :**

```
SELECT CHAR_LENGTH(NULL);
```

**输出:**

```
NULL
```

**2。ASCII()函数:**
在马里亚数据库中，ASCII 函数用于查找该字符串中最左边字符的 ASCII 值。在这个函数中，一个字符串将作为参数传递，它将返回最左边字符的 ASCII 值。

**语法:**

```
ASCII(single_character)
```

**参数:**必选。
**单字符:**如果超过一个字符将被通过，那么它将忽略除第一个字符之外的所有字符。

**示例-1 :**

```
SELECT ASCII('GeeksForGeeks');
```

**输出:**

```
107
```

**例-2 :**

```
SELECT ASCII('G');
```

**输出:**

```
107
```

**例-3 :**

```
SELECT ASCII('g');
```

**输出:**

```
147
```

**例-4 :**

```
SELECT ASCII('7');
```

**输出:**

```
55
```