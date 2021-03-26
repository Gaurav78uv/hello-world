#include<stdio.h>  // Dates (latest first) //
struct date
{int d;
int m;
int y;
};
int main()
{int N;
scanf("%d",&N);
int i,j,temp[3];
struct date arr[N];
for(i=0;i<N;i++)
{
scanf("%d/%d/%d",&arr[i].d,&arr[i].m,&arr[i].y);}

for(i=0;i<(N-1);i++)
{for(j=0;j<(N-1-i);j++)
{if((arr[j].y > arr[j+1].y )||((arr[j].y == arr[j+1].y ) && (arr[j].m > arr[j+1].m ))||((arr[j].y == arr[j+1].y ) && (arr[j].m ==arr[j+1].m )&&(arr[j].d > arr[j+1].d)))
 {temp[0]=arr[j].d;
  arr[j].d=arr[j+1].d;
  arr[j+1].d=temp[0];
  temp[1]=arr[j].m;
  arr[j].m=arr[j+1].m;
  arr[j+1].m=temp[1];
  temp[2]=arr[j].y;
  arr[j].y=arr[j+1].y;
  arr[j+1].y=temp[2];
 }}}
for(i=(N-1);i>=0;i--)
{printf("%d/%d/%d\n",arr[i].d,arr[i].m,arr[i].y);
}}
