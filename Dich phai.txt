#include<stdio.h>
#include<math.h>
int main(){
	int arr[100],n,i,right;
	scanf("%d",&n);
	for(i=0;i<n;i++){
		scanf("%d",&arr[i]);
	}
	scanf("%d",&right);
	for(i=n-right;i<n;i++){
		printf("%d ",arr[i]);
	}
	for(i=0;i<n-right;i++){
		printf("%d ",arr[i]);
	}
	return 0;
}