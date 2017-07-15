---
layout: post
title:  "Test pour la coloration syntaxique python"
date:   2017-07-14 22:25:00 +0200
category: python
---

# Test pour la coloration syntaxique en Python

```python

myfile = open("unesco.txt", "r")
s = myfile.read().lower()
myfile.close()
print(s)

print("Nb char : ", len(s))

myfile = open("newtext.txt", "w")
myfile.write(s[-250:][::-1])

myfile.write(s[::25])

squaretext = ""
for i in range(1,25,1):
	squaretext += str(i**2)
myfile.write(squaretext)
print(squaretext)
print("Number of char" , len(squaretext))

D = [2,9,12,16,24,28]
D2 = []
for i in D:
	for j in range(i):
		D2.append(i)
print("Length of D2 : " , len(D2))

D3 = []
for i in range(1,60+1):
	for j in range(i):
		D3.append(i)
print("Length of D3 : " , len(D3))
print("Sum of D3 : " , sum(D3))

```