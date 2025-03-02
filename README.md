#include<stdio.h>
int main()
{
        int f(int x,int n);
        int g(int x,int n);
        int p(int a[],int n);
        int q(int a[],int n);
        int n,l,i;
        int a[100],b[100],c[100];
        scanf("%d %d",&n,&l);
        for(i=0;i<n;i++)
        {
                scanf("%d",&a[i]);
        }
        for(i=0;i<n;i++)
        {
                b[i]=f(a[i],l);
        }
        for(i=0;i<n;i++)
        {
                c[i]=g(a[i],l);
        }
        int x,y;
        x=p(b,n);
        y=p(c,n);
        printf("The min time is: %d\n",x);
        printf("The max time is: %d",y);
        return 0;
}
int f(int x,int n)
{
        int y,a,b;
        a=x;
        b=n-x;
        if(a>=b) y=b;
        else y=a;
        return(y);
}
int g(int x,int n)
{       
        int y,a,b;
        a=x;
        b=n-x;
        if(a>=b) y=a;
        else y=b;
        return(y);
}
int p(int a[],int n)
{
        int max=a[0],i=0;
        for(i=0;i<n;i++)
        {
                if(a[i]>max)
                        max=a[i];
        }
        return(max);
}
