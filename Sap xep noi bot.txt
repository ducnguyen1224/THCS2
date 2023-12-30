#include <stdio.h>
int bubblesort(int a[], int n){
	for(int i=0;i<n-1;i++){
		int ok=0;
		for(int j=0;j<n-i-1;j++){
			if(a[j]>a[j+1]){
				int tmp=a[j];
				a[j]=a[j+1];
				a[j+1]=tmp;
				ok=1;
			}
		}
		if(ok==0) break;
			printf("Buoc %d: ",i+1);
		for(int k=0;k<n;k++) printf("%d ",a[k]);
		printf("\n");
		
	}
}
int main() {
	int n;
	scanf("%d", &n);
	int a[n];
	for(int i=0;i<n;i++){
		scanf("%d", &a[i]);
	}
	bubblesort(a,n);
//	for(int i=0;i<n;i++){
//		printf("%d ", a[i]);
//	}
 }