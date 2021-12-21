# MS 接入中的秒()和时间()功能

> 原文:[https://www . geesforgeks . org/ms-access 中的秒和时间函数/](https://www.geeksforgeeks.org/second-and-time-function-in-ms-access/)

**1。第二个()函数:**
在 MS Access 中，第二个()函数返回日期时间的第二部分。在此函数中，日期时间将作为参数传递，并将返回日期时间的第二部分。返回的整数将在 0 到 59 的范围内。

**语法:**

```
Second(time)
```

**示例-1 :**

```
SELECT Second(#12:28:45#);
```

**输出–**

```
45 
```

**示例-2 :**

```
SELECT Second(#14/09/2020 11:19:54 PM#);
```

**输出–**

```
54
```

**2。Time()函数:**
在 MS Access 中，Time()函数返回当前计算机系统时间。在这个函数中，不会传递任何东西，它将返回当前时间。

**语法:**

```
Time()
```

**示例-1 :**

```
SELECT Time() ;
```

**输出–**

```
10:56:47 AM
```

**示例-2 :**

```
SELECT Time() ;
```

**输出–**

```
10:57:36 AM
```