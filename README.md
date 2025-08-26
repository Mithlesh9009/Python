def is_even(num):
    if num%2 == 0:
        return "even"
    return "odd"
print(is_even(10))

def is_prime(num,count= 0):
    for val in range(1,num+1):
        if num%val == 0:
            count = count+1
    if count == 2:
        return 'prime'
    return 'non prime'
num = 13
print(is_prime(num))

def factorial (num,fact = 1):
    if  num > 0:
        for val in range(1,num+1):
            fact = fact*val
        return fact
    return"not possible"
num = 5
print(factorial(num))

def addall (num,total=0):
    while num!=0:
        rem = num % 10
        total = total + rem
        num = num//10
    return total
num = 2467
print(addall(num))

def addall (num,total=0):
    temp = num
    if num < 0:
        num = num*(-1)
    else:
        num = num
    while num!=0:
        rem = num % 10
        total = total + rem
        num = num//10

    if temp < 0:
        return total *(-1)
    return total
num = -2467
print(addall(num))

def armstrong(num,power,sum = 0):
    original = num
    while num != 0:
        rem = num % 10
        sum = sum+rem ** power
        num = num//10
    if sum == original:
        return 'Armstrong'
    return 'not a armstrong'
num = 153
power = len(str(num))
print(armstrong(num,power))

def armstrong(num,power,sum = 0):
    while num != 0:
        rem = num % 10
        sum = sum+rem ** power
        num = num//10
    return sum
num = 370
power = len(str(num))
if (armstrong(num,power))  == num:
    print("armstrong")
else:
    print("not armstrong")

def armstrong(num,power,sum = 0):
    while num != 0:
        rem = num % 10
        sum = sum+rem ** power
        power =power-1
        num = num//10
    return sum
num = 135
power = len(str(num))
if (armstrong(num,power))  == num:
    print("disarm number")
else:
    print("not disarm number")

def reversiable(num,rev = 0):
    while num!= 0:
        rem = num%10
        rev = rev*10+rem
        num = num//10
    return rev
num = 9109538828
print(reversiable(num))

def binary(num,val = 0,place = 1):
    while num!= 0:
        rem = num%2
        val = val+rem*place
        place = place*10
        num = num // 2
    return val
num = 24
print(binary(num))

def number(num,val = 0,place = 0):
    while num != 0:
        rem = num % 10
        val = val +rem*2 ** place
        place = place +1
        num = num // 10
    return val
num = 11011
print(number(num))


def prime(num,count= 0):
    for val in range(1,num+1):
        if num % val == 0:
            count = count+1
    return count == 2
def palindrom(num,val=0):
    temp = num
    while num!= 0:
        rem = num%10
        val = val*10+rem
        num = num//10
    return temp == val
def palyprime(num):
    if palindrom(num) and prime(num):
        return "palyprime"
    return "not palyprime"

num = 11
print(palyprime(num))

def prime(num,count= 0):
    for val in range(1,num+1):
        if num % val == 0:
            count = count+1
    return count == 2
def palindrom(num,val=0):
    temp = num
    while num!= 0:
        rem = num%10
        val = val*10+rem
        num = num//10
    return temp == val
def EMIRP(num):
    result = palindrom(num)
    if prime(num) and result != num and palindrom(num) == prime(result):
        return "EMIRP"
    return "not EMIRP"

num = 13
print(EMIRP(num))

def strong (num,value = 0):
    temp = num
    while num != 0:
        rem = num %10
        fact = 1
        for val in range(1,rem+1):
            fact = fact*val
        value = value + fact
        num = num//10
    if temp == value:
        return "strong number"
    return "weak number"
num = 145
print(strong(num))

def addsq(num,val = 0):
    while num != 0:
        rem =  num %10
        val = val +rem ** 2
        num = num //10
    return val
def Happy(num):
    while num > 9:
        num = addsq(num)
    if num == 1 or num == 7:
        return 'Happy number'
    return 'sad number'
num = 19
print(Happy(num))

def lcm(num1,num2):
    if num1 > num2:
        res = num1
    else:
        res = num2
    while True:
        if res % num1 == 0 and  res % num2 == 0:
            return res
        res = res+1
num1 = 10
num2 = 5
print(lcm(num1,num2))

def Gcd(num1,num2):
    if num1 > num2:
        res = num1
    else:
        res = num2
    while res != 0:
        if num1 % res == 0 and num2 % res == 0:
            return res
        res = res-1
num1 = 24
num2 = 21
print(Gcd(num1,num2))

print((lambda num1,num2: num1+num2)(7,5))

def sq(num):
    return num ** 2
print(list(map(sq,range(1,11))))

def is_even(num):
        if num % 2 == 0:
            return F'{num} is even'
        return F'{num} is odd'
print(list(map(is_even,range(1,11))))

def is_prime(num,count = 0):
    for val in range(1,num+1):
        if num% val == 0:
            count = count+1
    if count == 2:
        return f'{num} is prime'
    return f'{num} is not prime'
mapobj = (map(is_prime, range(1, 11)))
for ans in mapobj:
    print(ans)

def arm(num,total= 0):
    power = len(str(num))
    temp = num
    while num != 0:
        rem = num%10
        total = total+rem ** power
        num =num//10
    if total == temp:
        return f'{temp} is armstrong'
    return f'{temp} is not armstrong'
print(list(map(arm,range(1,15))))
def add2(T1,T2):
    return T1+T2
print(list(map(add2,(5,6,7,8,9),(10,20,30,40,50))))
print(list(map(lambda n1 : n1**2,range(5,10))))
print(list(map(lambda n1,n2:n1+n2,(5,6,7,8,9),(10,20,30,40,50))))

print(list(map(lambda n1:"even number" if n1 % 2 == 0 else "odd number",range(1,10))))
n = 4
print('\n'.join(list(map(lambda st :'* '*n,range(1,n+1)))))
n = 5
print('\n'.join(list(map(lambda st :'* '*st,range(1,n+1)))))
print('\n'.join(list(map(lambda st :'* '*st,range(n,0,-1)))))

print('\n'.join(list(map(lambda sp,st:'  '*sp+'* '*st,range(n,0,-1),range(1,n+1)))))
print('\n'.join(list(map(lambda st,sp:'  '*sp+'* '*st,range(n,0,-1),range(n+1)))))
n =4
print('\n'.join(list(map(lambda sp,st:'  '*sp+'* '*st,range(n,0,-1),range(1,n*2,2)))))

print(list(map(lambda ch : int(ch),input().split())))
def convert(ch):
    return ch
s = input("Enter a ele: ")
l = s.split()
print(list(map(convert,l)))

print(list(map(lambda a,b : a+b,list(map(int(input.split(),list(map(int(input.split())))))))))
def prime(num):
    if num > 1:
        for val in range(2,int(num**0.5)+1):
            if  num%val == 0:
                return False
            return True
    return False
print(list(filter(prime,range(1,51))))
def armstrong(num,sum = 0):
    temp = num
    power = len(str(num))
    while num != 0:
        rem = num % 10
        sum = sum+rem ** power
        num = num//10
    if temp == sum:
        return True
    return False
print(list(filter(armstrong,range(1,1001))))
print(list(map(lambda word: len(word)%2 == 0,input().split())))
def trail(num):
    print(num)
    num = num+1
    trail(num)
num = 1
trail(num)

n = 20
a = 0
b =1
for _ in range(n):
    print(a, end=' ')
    a,b = b,a+b

num = 12
a = 0
b = 1
count= 0
while count < num:
    print(a, end=" ")
    a, b = b, a + b
    count += 1

def trail(num):
    if num == 0:
        return
    print(num)
    trail(num-1)
num = 10
print(trail(num))

def is_even(num1,num2):
    if num1 == num2+1:
        return
    if num1%2 == 0:
        print(num1)
    return is_even(num1+1,num2)

num1 = 1
num2 = 78
is_even(num1,num2)


def factorial(num):
    if num == 0 or num == 1:
        return 1
    return num * factorial(num-1)
num = 5
print(factorial(num))

def add(num):
    if num == 0:
        return 0
    return (num%10)%2 == 0 + add(num//10)
num = 9109538828
print(add(num))

def armstrong(num,power):
    if num == 0:
        return 0
    return(num%10)** power+ armstrong(num//10,power)

num = 153
power = len(str(num))
if armstrong(num,power) == num:
    print("armstrong")
else:
    print("not armstrong")

def binary(num,place = 0):
    if num == 0:
        return 0
    return (num%10)*2**place+binary(num//10,place+1)

num = 11000
print(binary(num))

def integer(num,place = 1):
    if num == 0:
        return 0
    return (num%2)* place + integer(num//2,place*10)
num = 24
print(integer(num))



def factorial(num):
    if num == 0 or num == 1:
        return 1
    return num * factorial(num-1)
def sum_of_num(num):
    if num == 0:
        return 0
    return factorial(num%10)+ sum_of_num(num//10)
def strong(mum):
    if sum_of_num(num) == num:
        return"Strong"
    return "Weak"
num = 145
print(strong(num))

def prime(num,val,count=0):
    if val == num+1:
        return 0
    if num% val == 0:
        return 1+ prime(num,val+1)
    else:
        return 0+ prime(num, val+1)
num = 5
val = 1
print("prime" if prime(num,val) == 2 else "not prime")
def reverse(num,place):
    if num == 0:
        return 0
    return (num%10)*place +reverse(num//10,place//10)
num = 456
place = 10**(len(str(num))-1)
print(reverse(num,place))
def prime(num,val=1):
    if val == num+1:
        return 0
    if num %val == 0:
        return 1 + prime(num,val+1)
    return 0 + prime(num,val+1)

def reverse(num,place):
    if num == 0:
        return 0
    return (num%10)*place + reverse(num//10,place//10)

def EMIRP(num):
    length = len(str(num))
    rev = reverse(num,10**(length-1))
    if prime(num) == 2 and rev != num and prime(rev) == 2:
        return "EMIRP"
    return "NOT"
num = 31
print(EMIRP(num))

def number(val,num =0):
    if val == 6:
        return num
    num = num+ val
    return number(val+1,num)
val = 1
print(number(val))

def fact(num):
    if num == 0:
        return 1
    return num * fact(num-1)
num = 6
print(fact(num))

def count_digit(num,count=0):
    if num == 0:
        return count
    count += 1
    return count_digit(num//10,count)
num = 5694567
print(count_digit(num))

row  = 5
for r in range(1,row+1):
    for c in range(1,row+1):
        print('*',end=" ")
    print()

row  = 4
for r in range(1,row+1):
    for c in range(1,2*row+1):
        print('*',end=" ")
    print()
row  = 5
for r in range(1,row+1):
    for c in range(1,r+1):
        print('*',end=" ")
    print()

row  = 5
for r in range(1,row+1):
    for c in range(r,row+1):
        print('*',end=" ")
    print()


row  = 5
space = row-1
for r in range(1,row+1):
    for c in range(1,space+1):
        print(' ',end=" ")
    for st in range(1,r+1):
        print('*',end=" ")
    print()
    space -= 1

row  = 5
space = 1
for r in range(1,row+1):
    for c in range(1,space):
        print(' ',end=" ")
    for st in range(r,row+1):
        print('*',end=" ")
    print()
    space += 1

row = 4
space = row - 1
star = 1
for line in range(1,row+1):
    for sp in range(1,space+1):
        print(' ',end =" ")
    for st in range(1,star+1):
        print('*',end=' ')
    print()
    star += 2
    space -=1

row = 4
for line in range(1,row+1):
    for sp in range(row-line):
        print(' ',end =" ")
    for st in range(line*2-1):
        print('*',end=' ')
    print()

row =4
space = 1
star = row-1
for line in range(1,row+1):
    for sp in range(1,space+1):
        print(' ',end=' ')
    for st in range(star*2+1):
        print('*',end=' ')
    print()
    space +=1
    star -=1


row = 4
for line in range(row,0,-1):
    for sp in range(row-line):
        print(' ',end=' ')
    for st in range(line*2-1):
        print('*',end=' ')
    print()

row = 4
for line in range(1,row+1):
    for sp in range(row-line):
        print(' ',end =" ")
    for st in range(line*2-1):
        print('*',end=' ')
    print()
for line in range(row-1, 0, -1):
    for sp in range(row - line):
        print(' ', end=' ')
    for st in range(line * 2 - 1):
        print('*', end=' ')
    print()

num = 7
space = num-2
star = 1
for row in range(1,num+1):
    for sp in range(1,space+1):
        print(' ',end=' ')
    for st in range(1,star+1):
        print('*',end=' ')
    print()
    if row<num//2+1:
        space -= 1
        star += 2
    else:
        space +=1
        star -=2

num = 5
star = 1
for row in range(1,num+1):
    for st in range(1,star+1):
        print('*',end=' ')
    print()
    if row<num//2+1:
        star +=1
    else:
        star-=1

num = 5
star =1
space = num-2
for row in range(1,num+1):
    for sp in range(1,space+1):
        print(' ',end=' ')
    for st in range(1,star+1):
        print('*',end=' ')
    print()
    if row <num //2+1:
        space-= 1
        star +=1
    else:
        space +=1
        star -=1

num = 5
space =1
star = num
for row in range(1,num+1):
    for sp in range(space):
        print(' ',end=' ')
    for st in range(1,star+1):
        print('*',end=' ')
    print()
    if row < num//2+1:
        space += 1
        star -= 2
    else:
        space -= 1
        star += 2

num = 5
row = 1
while row != num+1:
    col = 1
    while col< 2*num+1:
        print('*',end=' ')
        col = col+1
    print()
    row = row+1

num = 5
row = num
while row != 0:
    col = 1
    while col <= row:
        print('*',end= ' ')
        col =col+1
    print()
    row = row-1

num = 5
row = num
while row != 0:
    sp = 1
    while sp<row:
        print(' ',end=' ')
        sp = sp+1
    col = row
    while col < num+1:
        print('*',end=' ')
        col = col+1
    print()
    row=row-1

num = 5
row =num
while row !=0 :
    sp = row
    while sp< num:
        print(' ',end= ' ')
        sp = sp+1
    col = 1
    while col < row+1:
        print('*',end=' ')
        col = col+1
    print()
    row = row-1

num = 4
row = 1
while row < num+1:
    sp = row
    while sp< num :
        print(' ',end= ' ')
        sp = sp+1
    col = 1
    while col<= 2*row-1:
        print('*',end=' ')
        col = col+1
    print()
    row = row+1

num = 4
row = num
while row != 0:
    sp = row
    while sp< num:
        print(' ',end= ' ')
        sp = sp+1
    col = 1
    while col <= 2*row-1:
        print('*',end=' ')
        col = col+1
    print()
    row = row-1
num = 5
row = 1
space = num //2
star = 1
while row<=num:
    sp = 1
    while sp<=space:
        print(' ',end=' ')
        sp = sp+1
    st = 1
    while st <= star:
        print('*',end=' ')
        st = st+1
    print()
    if row < num//2+1:
        space -=1
        star +=2
    else:
        space +=1
        star -=2
    row = row+1

num = 5
row = 1
star = 1
while row <= num:
    st = 1
    while st<=star:
        print('*',end=' ')
        st =st+1
    print()
    if row< num//2+1:
        star += 1
    else:
        star -= 1
    row = row+1

num = 5
row = 1
space = num //2
star = 1
while row<=num:
    sp = 1
    while sp<=space:
        print(' ',end=' ')
        sp = sp+1
    st = 1
    while st <= star:
        print('*',end=' ')
        st = st+1
    print()
    if row < num//2+1:
        space -=1
        star +=1
    else:
        space +=1
        star -=1
    row = row+1

num = 5
row = 1
space =0
star = num
while row < num+1:
    sp =1
    while sp <= space:
        print(' ',end=' ')
        sp =sp+1
    st = 1
    while st <= star:
        print('*',end=' ')
        st =st+1
    print()
    if row < num//2+1:
        space += 1
        star -= 2
    else:
        space -=1
        star +=2
    row =row+1

num = 5
for row in range(1,num+1):
    for col in range(1,row+1):
        if col == 1 or row == num or row == col:
            print('*',end=' ')
        else:
            print(' ',end=' ')
    print()

num = 4
for row in range(1,num+1):
    for col in range(1,num+1):
        if row ==1 or row == num or col == 1 or col == num:
            print('*',end=' ')
        else:
            print(' ',end=' ')
    print()

num = 5
for row in range(1,num+1):
    for col in range(1,row+1):
        print(col,end=' ')
    print()

num = 5
for row in range(num,0,-1):
    for col in range(1,row+1):
        print(col,end=' ')
    print()


num = 5
for row in range(1,num+1):
    for val in range(row,0,-1):
        print(val,end=' ')
    print()

num = 5
for row in range(1,num+1):
    for val in range(num,num-row,-1):
        print(val,end=' ')
    print()

num = 5
for  row in range(1,num+2):
    for sp in range(num -row+1):
        print(' ',end=' ')
    for val in range(1,row):
        print(val,end=' ')
    print()

num = 3
while num >=10:
    total= 0
    while num != 0:
        rem = num%10
        total = total+rem**2
        num = num//10
    num = total
if num == 1 or num ==7:
    print("happy")
else:
    print("sad")


num = 5
for row in range(1,num+1):
    for sp in range(row-1):
        print(' ',end=' ')
    for val in range(row,num+1):
        print(val,end=' ')
    print()

num = 5
for row in range(1,num+1):
    for ele in range(num,num-row,-1):
        print(ele,end=' ')
    print()

num = 5
space = num -1
for row in range(1,num+1):
    for sp in range(1,space+1):
        print(' ',end=' ')
    for val in range(1,row+1):
        print(val,end=' ')
    print()
    space = space-1

num = 5
space  =  num-1
for row in range(num,0,-1):
    for sp in range(1,space+1):
        print(' ',end=' ')
    for val in range(row,num+1):
        print(val,end=' ')
    print()
    space -= 1
num = 1234
place = 10**(len(str(num))-1)
rev =0
while num !=0:
    rem = num%10
    rev = rev+rem*place
    place = place//10
    num = num//10
print(rev)

num = 1234
place = 10
rev =0
while num !=0:
    rem = num%10
    rev = rev*place+rem
    num = num//10
print(rev)

num = 13
total = 0
for val in range(1,num+1):
    if num%val == 0:
        total += 1
if total == 2:
    temp = num
    result = 0
    while num != 0:
        rem = num%10
        result = result*10+rem
        num = num//10
    if temp != result:
        count = 0
        for val1 in range(1,result+1):
            if result% val1 == 0:
                count += 1
        if count == 2:
            print("EMTRP")
        else:
            print("not EMIRP")
    else:
        print("not EMIRP")
else:
    print("not EMIRP")

num = 19
while num > 9:
    res = 0
    while num!=0:
        rem =  num%10
        res = res+rem*rem
        num=num//10
    num = res
if num == 1 or num == 7:
    print("happy")
else:
    print("not happy")

num = 4
for row in range(1,num+1):
    for  space in range(num-row):
        print(' ',end= ' ')
    for val in range(1,row*2):
        print(val,end=' ')
    print()

num = 4
for row in range(num,0,-1):
    for  space in range(num-row):
        print(' ',end= ' ')
    for val in range(1,row*2):
        print(val,end=' ')
    print()
num = 4
space = num-1
values = 1
ele = 1
for row in range(1,num+1):
    for  space in range(1,space+1):
        print(' ',end= ' ')
    for val in range(values):
        print(ele,end=' ')
    print()
    space -=1
    values += 2
    ele += 1

def factorial(num):
    if num == 0 or num == 1:
        return 1
    return num * factorial(num-1)
def sum_fact(num):
    if num == 0:
        return 0
    return factorial(num%10)+sum_fact(num//10)
def strong(num):
    if sum_fact(num) == num:
        return 'strong'
    return 'weak'

num = 145
print(strong(num))


def factorial(num):
    if num == 0 or num == 1:
        return 1
    return num * factorial(num-1)
def strong(num):
    if num == 0:
        return 0
    return factorial(num%10)+strong(num//10)

num =145
if (strong(num)) == num:
    print('strong')
else:
    print("not strong")

def prime(num,val =1):
    if val == num+1:
            return 0
    if num%val == 0:
        return 1 + prime(num,val+1)
    return 0 +prime(num,val+1)
def palindrom(num,place):
    if num == 0:
        return 0
    return (num%10)*place+palindrom(num//10,place//10)
def EMIRP(num):
    rev = palindrom(num,place = 10**(len(str(num))-1))
    if prime(num)==2 and rev != num and prime(rev) == 2:
        return "EMIRP"
    return "NOT EMIRP"
num = 13
print(EMIRP(num))

s = 'abcde'
res =''
for ch in range(len(s)-1,-1,-1):
    res = res+s[ch]
print(res)

s = 'ABCDE'
res = ''
ind = len(s)-1
while ind > -1:
    if s[ind] in s:
        res = res+s[ind]
    ind -= 1
print(res)

s = 'abccba'
for ch in range(0,len(s)//2):
    if s[ch] != s[-(ch+1)]:
        print('not palindrome')
        break
else:
    print('palindrom')

s = 'aaabbccccdd'
count= 1
res =''
for ind in range(0,len(s)-1,1):
    if s[int(ind)] == s[int(ind+1)]:
        count = count+1
    else:
        res += str(count)+s[int(ind)]
        count = 1
res += str(count)+s[int(ind)]
print(res)

s = 'refer'
l = []
for si in range(0,len(s)):
    for ei in range(si+1,len(s)+1):
        word= s[si:ei]
        if word == word[::-1]:
            print(word)
s = 'refer'
l = []
for si in range(0,len(s)):
    for ei in range(si+1,len(s)+1):
        word= ''
        for ind in range(si,ei):
            word = word+s[ind]
        # print(word)
        rev = ''
        for ch in word:
            rev = ch +rev
        # print(word,rev)
        if word == rev:
            print(word)
s = 'refer'
for si in range(0,len(s)):
    for ei in range(si+1,len(s)+1):
        word= ''
        for ind in range(si,ei):
            word = word+s[ind]
        # print(word)
        rev = ''
        for ch in word:
            if word.count(ch)>1:
                break
        else:
            print(word)

num = 123
count = 0
fact = 1
while num !=0:
    rem =  num%10
    count = count+rem
    fact =fact*rem
    num = num//10
if count == fact:
    print("spy")
else:
    print('not spy')


num = 6
val = 1
sum_fact = 0
while val != num//2+1:
    if num% val ==0:
        sum_fact += val
    val = val+1
if sum_fact == num:
    print("perfect number")
else:
    print("not perfect number")

num = 6
sum_fact = 0
for val in range(1,num//2+1):
    if num% val ==0:
        sum_fact += val
    val = val+1
if sum_fact == num:
    print("perfect number")
else:
    print("not perfect number")


num = 27
place = 1
binary = 0
while num!=0:
    rem = num%2
    binary = binary+rem*place
    place = place*10
    num = num//2
print(binary)


num = 11011
place = 0
integer = 0
while num!=0:
    rem = num%10
    integer = integer+rem*(2**place)
    place = place+1
    num = num//10
print(integer)
print(bin(29))

num = 29
count = 0
while num!=0:
    rem = num%2
    if rem%2 == 1:
        count += 1
    num = num//2
if count %2 == 0:
    print("evil")
else:
    print("odious")


n1 = 18
n2 = 24
if n1> n2:
    gcd = n1
else:
    gcd = n2
while True:
    if n1%gcd == 0 and n2%gcd == 0:
        print(gcd)
        break
    gcd -=1

n1 = 10
n2 = 5
if n1> n2:
    LCM = n1
else:
    LCM = n2
while True:
    if LCM%n1 == 0 and LCM%n2 == 0:
        print(LCM)
        break
    LCM+=1

num = 4
for val in range(1,num+1):
    for col in range(1,2*num+1):
        print('*',end=' ')
    print()

num = 4
row = 1
while row < num+1:
    col = 1
    while col < 2*num+1:
        print('*',end=' ')
        col = col+1
    print()
    row = row+1

num = 5
for row in range(1,num+1):
    for col in range(1,row+1):
        print('*',end= ' ')
    print()

num = 5
row = 1
while row < num+1:
    col = 1
    while col < row+1:
        print("*",end=' ')
        col = col+1
    print()
    row =row+1

num = 5
for row in range(num,0,-1):
    for col in range(1,row+1):
        print('*',end= ' ')
    print()

num = 5
row = num
while row != 0:
    col = row
    while col != 0:
        print("*",end=' ')
        col = col-1
    print()
    row =row-1

num = 5
for row in range(1,num+1):
    for sp in range(num-row):
        print(' ',end=' ')
    for st in range(1,row+1):
        print('*',end=' ')
    print()

s = 'engineering'
res = ''
ind= 0
while ind != len(s):
    if s[ind] not in res:
        res = res+s[ind]
        ind +=1
    print(res)
    ind +=1


s = 'engineering'
res =''
count = 0
for ch in s:
    if ch not in res:
        res = res + ch
        for ch in res:
            count = count +1
        print(f'{ch}:{s.count(ch)}')

s = 'engineering'
res =''
ind = 0
while ind !=len(s):
    if s[ind] not in res:
        res += s[ind]
    ind += 1
for ch in res:
    print(f'{ch}:{s.count(ch)}')

s = 'aaaabbccccdd'
res= ''
count = 1
ind = 0
while ind != len(s)-1:
    if s[ind] == s[ind+1]:
        count += 1
    else:
        res += str(count)+s[ind]
        count = 1
    ind += 1
res += str(count)+s[ind]
print(res)

s = 'racecar'
l = []
for si in range(0,len(s)+1):
    for ei in range(si+1,len(s)-1):
        word = ''
        for ind in range(si,ei):
            word= word+s[ind]
            l.append(word)
        print(word)

s = 'rever'
for si in range(0,len(s)):
    for ei in range(si+1,len(s)-1):
        word = s[si:ei]
        for ch in word:
            if word.count(ch)>1:
                break
        else:
            print(word)



s ='i will give mock today'
word = ''
l = []
for ch in s:
    if ch == ' ':
        l = l+[word]
        word =''
    else:
        word = word+ch
l = l+[word]
print(l)
0
def factors(num):
    if num == 0 or num == 1:
        return 1
    return num*factors(num-1)
def strong(num):
    if num == 0:
        return 0
    return factors(num%10)+strong(num//10)
num = 145
print(strong(num))


def total(num):
    if len(num)%2 == 0:
        return num

num=input().split(' ')
print(list(filter(total,num)))

def prime(num):
    if num>1:
        for val in range(2,int(num**0.5)+1):
            if num%val == 0:
                return False
            return True
    return False
print(list(filter(prime,range(0,101))))

print(list(filter(lambda word : len(word)%2 == 0,input().split(' '))))
def add_sq(num,res=0):
    while num !=0:
        rem = num%10
        res = res+rem*rem
        num = num//10
    return res
def happy(num):
    while num>9:
        num = add_sq(num)
    if num == 1 or num == 7:
        return 'Happy number'
    return 'not happy number'
num = 19
print(happy(num))

def add_Sq(num,sum_fact=0):
    while num!=0:
        rem = num%10
        fact = 1
        for val in range(1,rem+1):
            fact =  fact*val
        sum_fact += fact
    num = num//10
    return sum_fact
def strong(num):
    if sum_fact == num:

num = 4
space = num-1
star = 1
for row in range(1,num+1):
    for sp in range(1,space+1):
        print(' ',end=' ')
    for st in range(1,star+1):
        if st == 1 or row == num or st == star:
            print('*',end=' ')
        else:
            print(' ',end=' ')
    print()
    space -= 1
    star += 2


s = 'abcde'
res = ''
for ind in range(-1,-len(s)-1,-1):
    res = res+s[ind]
print(res)

s = 'abcde'
res = ''
for ind in range(len(s)-1,-1,-1):
    res = res+s[ind]
print(res)

s = 'mnopqrs'
res = ''
for ch in s:
    res = ch+res
print(res)

s = 'kmomk'
for ind in range(0,len(s)//2):
    if s[ind] != s[-(ind-1)]:
        print('not palindrome')
        break
else:
    print('palindrome')

s = 'engineering'
res = ''
for ch in s:
    if ch not in res:
        res = res+ch
        for ch in res:
            s.count(ch)
        print(f'{ch}={s.count(ch)}')


row = int(input('Enter the number of rows: '))
column = int(input('Enter the number of columns: '))
Matrix = []
for r in range(1,row+1):
    elements = []
    for col in range(1,column+1):
        elements.append(int(input('Enter the element: ')))
    Matrix.append(elements)
print(Matrix)
row = int(input('Enter the number of rows: '))
column = int(input('Enter the number of columns: '))
matrix = [[int(input('Enter value: ')) for col in range(1, column+1)] for r in range(1, row+1)]
print(matrix)

l = [3,4,0,1,6,-1,8,7]
target = 7
for si in range(len(l)):
    for ei in range(si+1,len(l)):
        subl = []
        sub_digit =0
        for ind in range(si,ei):
            subl += [l[ind]]
            sub_digit += l[ind]
        if sub_digit == target:
            print(subl)


m1 = [[1,2,3],[3,4,5]]
m2 = [[4,5,1],[2,3,2]]
if len(m1)==0 and len(m2) == 0:
    print([])
elif len(m1) == len(m2) and len(m1[0]) == len(m2[0]):
    for ind1  in range(1,len(m1)+1):
        for ind2 in range(1,len(m2[0])+1):
           m1[ind1]= (m1[ind1]+[ind2]+ m2[ind1]+[ind2])
        print(m1)

else:
    print('n/a')

m1 = [[4,2],[5,4]]
m2 = [[0,6],[4,7]]
if len(m1) == 0 and len(m2) ==0:
    print([])
elif len(m1) == len(m2) and len(m1[0])==len(m2[0]):
    res = []
    for line in range(len(m1)):
        rs = []
        for col in range(len(m2[0])):
            sum = 0
            for row in range(len(m2)):
                sum += m1[line][row]*m2[row][col]
            rs.append(sum)
        res.append(rs)
    print(res)
else:
    print('notpossible')

s = 'engineering'
print({s[ind]:s.count(s[ind]) for ind in range(len(s)) if ind%2 != 0})
print({ch:'even' if ch%2 == 0 else 'odd' for ch in range(1,10)})




