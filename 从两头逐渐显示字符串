#include<stdio.h>
#include<string.h>
//从两头逐渐显示字符串
int main(void)
{
	char arr1[]=“welcome to be here!!!!”;
	char arr2[]=“######################”;
int left = 0;
int right = strlen(arr1)-1; //int right = sizeof(arr1)/sizeof(arr1[0])-2;
while(left<=right)          //因为使用sizeof还会考虑字符串最后的\n转义字符
{                           //{1,2,3,4,5,\n}        要想让右下标对应5这个字符，必须让6-2
arr2[left]=arr1[left];      //{0,1,2,3,4,5 }
arr2[right]=arr1[right];
printf(“%s\n”,arr2);//可以加上Sleep(1000);休息1000ms也就是1s，但是要加上头文件#include<windows.h>
left++;
right--;
}
return 0;
}
