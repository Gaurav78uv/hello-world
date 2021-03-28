#include<stdio.h>  // Round F 2020 (1st problem) //
int main()
{int n,k,i,j,a=0;
 scanf("%d %d",&n,&k);
 
 int arr[n],count[n];
 for(i=0;i<n;i++)
 {
 scanf("%d",&arr[i]);
}
for(i=0;;i++)
{for(j=0;j<n;j++)
{if(arr[j]!=0)
{
arr[j]=arr[j]-k;
if(arr[j]<=0)
{count[a]=j+1;
 arr[j]=0;
 a++;
}
}
}
if(a==n)
{break;
}
}
for(i=0;i<n;i++)
printf("%d ",count[i]);
 
}
