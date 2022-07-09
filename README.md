import math
n=int(input())
seive=[]
for i in range(n):
    seive=[True]*n
seive[0]=seive[1]=False 
x=int(math.sqrt(n))
for i in range(2,x+1):
    if seive[i]:
        for j in range(i*i,n,i):
            seive[j]=False
for i in range(n):
    if seive[i]:
        print(i,end=' ')
        
        
'''n=int(input())
seive=set(range(2,n+1))
while seive:
    prime=min(seive)
    print(prime,end=' ')
    seive-=set(range(prime,n+1,prime))
    '''
