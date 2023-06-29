# Yogurt
class case:
   def __init__(self,bought,limit_per_day,yogurt_expiration):
       self.bought=bought
       self.limit_per_day=limit_per_day
       self.yogurt_expiration=sorted(yogurt_expiration)
       self.consumed=0
   def consume(self):
       day=0
       consumed_today=0
       for i in range (self.bought):
           if consumed_today == self.limit_per_day:
               day+=1
               self.consumed=0
               if(yogurt_expiration[i]>day):
                   consumed_today+=1
                   self.consumed+=1
       return self.consumed
t=int(input())
while t:
    bought,limit_per_day=map(int,input().split())
    yogurt_expiration=(int,input().split())
    case=case(bought,limit_per_day)
    print(case.consume())
    t-=1
