---
layout: '../../layouts/PageLayout.astro'
title: iostream
description: My name is
relation:
  - basics
  - if-else
  - io
published: true
lang: misc
course: practice
order: 1
---

Write a basic program that holds 2 variables: `name` and `age`. The input `std::cin` should extract both name and age at the same time! The program should insert the following message into the console:
```
enter your name and age separated with a space:
> [name] [age]

my name is [name] and I am [age] year(s) old!
```

With the following input of `ethan 22`, you should expect the following output:

`my name is ethan and I am 22 years (s) old!`

## Possible Solutions:
### C++
```cpp
int age;
string name;
cout << "enter your name and age separated with a space: ";
cin >> name >> age;
cout << "my name is " << name << " and I am " << age << " year(s) old!\n";
```
### Python
```py
name, age = input("enter your name and age separated with a space: " ).split(' ', 2)
print("my name is ", name, " and I am ", age, " year(s) old!")
```