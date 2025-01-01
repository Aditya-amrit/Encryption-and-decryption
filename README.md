# Encryption-and-decryption

def encrypt(b, c):
    word = ''
    for n in b:
        if n in alp:
            position = alp.index(n)
            new_position = (position + c)
            word += alp[new_position]
    print(word)

def dycript(b, c):
    word = ''
    for n in b:
        if n in alp:
            position = alp.index(n)
            new_position = (position - c)
            word += alp[new_position]
    print(word)


alp = ['a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z']
a = input("What do you want to do type 'en' for encryption and 'dn' for decryption: ")
b = input("Enter the message: ")
c = int(input("Enter the number of shifts: "))
if c < len(alp):
    d=c - len(alp)
    c=int(d)

if a == 'en':
    encrypt(b, c)
elif a == 'dn':
    dycript(b,c)
else:
    print("Invalid Command!!")
