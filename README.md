# 14.previous-happy-number-of-a-given-number
def happ(n):
    s=0
    while(n!=0):
        r=n%10
        s=s+(r*r)
        n=n//10
    if s==1 or s==7:
        return True
    elif s==2 or s==3 or s==4 or s==5 or s==6 or s==8 or s==9:
        return False
    elif s>9:
        return happ(s)
n= int(input())
while(n>0):
    if (happ(n)):
        print(n)
        break
    n=n-1
