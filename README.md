#include<stdio.h>
void bubble_sort(int arr[],int sz)
{
	int i=0;
	for(i=0;i<sz-1;i++)		//sz-1是冒泡的趟数
	{
		int flag=1;
		int j=0;
		for(j=0;j<sz-i-1;j++)
		if(arr[j]>arr[j+1])
		{
			int tmp=arr[j];
			arr[j]=arr[j+1];
			arr[j+1]=tmp;
			flag=0;
		}
		else
		{
			continue;
		}
		if(flag==1)     //说明排序已经正确
		{
			break;
		}
	}
}

int main()
{
	int arr[]={8,9,7,6,4,4,3,8,1,0};
	int i=0;
	int sz=sizeof(arr)/sizeof(arr[0]);//必须写在函数前，写在函数内部会出问题
	bubble_sort(arr,sz);//arr传递到函数的是arr数组首个元素的地址
	for (i=0;i<sz;i++)
		printf(“%d”,arr[i]);
	return 0;
}
