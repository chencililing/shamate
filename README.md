#include <stdio.h>
#include <string.h>
int main ()
{
 char a[1000];
 char b[50];
 int num=0,j,i;
 printf("请输入想要查询的英文句子:\n");
 gets(a);
 printf("请输入想要统计的英文单词:\n");
 gets(b);
  
 for(i=0;i<strlen(a);i++)
 {
  strlwr(a);
  strlwr(b);
  for(j=0;j<strlen(b);j++)
  {
   if(a[i+j]!=b[j])
   {
   	break;
   }
  }
  if(j==strlen(b))
   {
    	num++;
   }
 }
  printf("你想要统计的单词个数为:%d\n",num); 
}
