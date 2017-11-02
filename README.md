# A-simple-problem

A simple problem

Problem Description

他很痴迷数学问题.。一天，我出了个数学题想难倒他，让他回答1 / n。但他却回答不了^_^. 请大家编程帮助他.

Input

第一行整数T，表示测试组数。后面T行，每行一个整数 n (1<=|n|<=10^5).

Output

输出1/n. (是循环小数的,只输出第一个循环节).

Sample Input

4 2 3 7 168

Sample Output

0.5 0.3 0.142857 0.005952380

代码：

#include<stdio.h>

#include<string.h>

char b[500001]={0};

int main()

{

    int t,i,d,n,s;
    
    scanf("%d",&t);
    
    while(t--)
    
    {
    
        memset(b,0,sizeof(b));
        
        scanf("%d",&n);
        
        if(n<0)
        
        {
        
            printf("-");
            
            n=-n;
            
        }
        

        if(n==1)
        
        {
        
            printf("%d\n",n);
            
            continue;
            
        }
        
        else
        
            printf("0.");
            
        d=1;b[0]=1;
        
        for(i=1;;i++)   
        
        {
        
            b[d]++;    
            
            s=d*10/n;   
            
            if(b[d]==2)
            
                break;      
                
            printf("%d",s);   
            
            d=d*10-s*n;
            
        }
        
        printf("\n");
        
    }
    
}

