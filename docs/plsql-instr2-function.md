# PLSQL | INSTR2 功能

> 原文:[https://www.geeksforgeeks.org/plsql-instr2-function/](https://www.geeksforgeeks.org/plsql-instr2-function/)

PLSQL INSTR2 函数用于使用 UCS2 代码点返回字符串中子字符串的位置。UCS-2 代码点是一种字符编码标准，其中字符由固定长度的 16 位(2 字节)表示。UCS-2 表示可能的最大长度为 65，536 个字符，或者从 0000h–FFFFh(2 字节)开始的十六进制数。

PLSQL INSTR2 函数在字符串中搜索用户使用字符指定的子字符串，并返回字符串中指定出现的子字符串的第一个字符的位置。PLSQL INSTR2 函数接受四个参数，即字符串、子字符串、起始位置和第 n 个外观。
字符串和子字符串可以是任何数据类型，如 CHAR、VARCHAR2、NCHAR、NVARCHAR2、CLOB 或 NCLOB。

**语法:**

```
INSTR2(string, substring [, start_position [, nth_appearance ]])
```

**使用的参数:**

*   **字符串–**用于指定需要搜索子字符串的字符串。它可以是任何数据类型 CHAR、VARCHAR2、NCHAR、NVARCHAR2、CLOB 或 NCLOB。
*   **子串–**用于指定需要搜索的子串。它可以是任何数据类型 CHAR、VARCHAR2、NCHAR、NVARCHAR2、CLOB 或 NCLOB。
*   **start _ position–**这是一个可选参数，用于指定字符串中搜索开始的位置。默认值为 1。INSTR2 函数从字符串的末尾开始计数到 start_position，如果插入的值为负，则向字符串的开头搜索。
*   **第 n 次出现–**是可选参数，用于指定子串的第 n 次出现。默认值为 1。

**支持的 Oracle/PLSQL 版本:**

1.  Oracle 12c
2.  Oracle 11g
3.  Oracle 10g
4.  Oracle 9i 发行版
5.  Oracle 8i 发行版

**示例-1:** 使用字符向前搜索来查找子串的位置。

```
DECLARE 
   Test_String string(20) := 'Geeksforgeeks';

BEGIN 
   dbms_output.put_line(INSTR2(Test_String, 'e')); 

END;  
```

**输出:**

```
2 
```

**示例-2:** 使用字符位置向前搜索来查找子串的位置。

```
DECLARE 
   Test_String string(20) := 'Geeksforgeeks';

BEGIN 
   dbms_output.put_line(INSTR2(Test_String, 'e', 1, 1)); 

END;  
```

**输出:**

```
2 
```

**示例-3:** 使用字符位置向前搜索来查找子串在第三个位置的位置。

```
DECLARE 
   Test_String string(20) := 'Geeksforgeeks';

BEGIN 
   dbms_output.put_line(INSTR2(Test_String, 'e', 1, 3)); 

END; 
```

**输出:**

```
10 
```

**示例-4:** 使用字符位置向后搜索来查找子串的位置。

```
DECLARE 
   Test_String string(20) := 'Geeksforgeeks';

BEGIN 
   dbms_output.put_line(INSTR2(Test_String, 'e', -2, 1)); 

END; 
```

**输出:**

```
11 
```

**示例-5:** 使用三字节字符集查找子字符串的位置。

```
DECLARE 
   Test_String string(20) := 'Geeksforgeeks';

BEGIN 
   dbms_output.put_line(INSTR2(Test_String, 'for', 1, 1)); 

END;  
```

**输出:**

```
6 
```