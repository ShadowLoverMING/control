# control

# control 1
```
#include<stdio.h>
int main()
{ int i,m[5],sum=0;
  for ( i=0; i<5; i++ )
    { scanf("%d", &m[i]);
      sum += m[i];
      printf("***m[%d]=%d\n",i,m[i]);
    }
  printf("%d\n",sum);
}
```

# control 2
```
#include<stdio.h>
int main()
{ int m[6]={0};
  int i,sum=0;
  for ( i=0; i<6; i++ )
    { 
      sum += m[i];
      printf("%d\n",m[i]);
    }
  printf("%d\n",sum);
}
```

# control 3
```
#include<stdio.h>
#define N 10
int main()
{ int a[N],sum=0;
  float average;
  for(int i=0; i<N;i++)  /*数组输入*/
   { scanf("%d",&a[i]);
     sum+=a[i];
   }
  average=1.0*sum/N; /*求平均数*/
  printf("average=%f\n",average);
  for(int j=0; j<N;j++)
   { if(a[j]>average) /*找数并输出*/
        printf("%d ",a[j]);
   }
  return 0;
}
```

# control 4
```
#include <stdio.h>
int main( )
{ int a[5] = { 10, 20, 30, 40, 50 };
  int i=3;
  while ( --i>=0 )
    printf("a[%d]=%d\t", i, a[i]); /* 循环变量i作数组下标 */
  return 0; 
}
```

# control 5
```
#include<stdio.h>
#define N 10
int main()
{
    int s,i,j,tmp;
    int a[10]={78,56,38,99,81,86,39,100,49,78};
    for( i=0; i<10;i++)
     printf("%d  ",a[i]);
    printf("\n");
    for( i=0; i<N-1;i++)
      { s=i;
        for( j=i+1;j<10;j++)
           if(a[s]>a[j]) 
             s=j;
        if(s!=i)
          {tmp=a[s];
           a[s]=a[i];
           a[i]=tmp;
          }
      }
    for( i=0; i<10;i++)
     printf("%d  ",a[i]);
  return 0; 
 }
 ```
 
 # control 6
 ```
 #include <stdio.h>
#define NUM 20
int  main( )
{    int a[NUM]={1, 1};
    int j;
    for (j=2; j<NUM; ++j)
        a[j] = a[j-1]+a[j-2];
    for ( j=0; j<NUM; j++)
        printf("%10d", a[j]);
}
```
