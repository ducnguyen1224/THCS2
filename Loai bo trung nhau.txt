#include<stdio.h>

int main()
{
	int n,i,j,a[250],k;
	scanf("%d",&n);
	for(i=0;i<n;i++)
		scanf("%d",&a[i]);	
	for(i=0;i<n-1;i++)
	{
		for(j=i+1;j<n;j++)
		if(a[i]==a[j])
			{
				for(k=j+1;k<n;k++)
				{
					a[k-1]=a[k];
				}
				n--;
				i--;	
			}
	}	
	for(i=0;i<n;i++)
		printf("%d ",a[i]);
	return 0;
}