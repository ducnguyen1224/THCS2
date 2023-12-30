#include<stdio.h>
#include<math.h>
int b[10099];
main(){
	int t;
	scanf("%d",&t);
	for(int i=2;i<10009;i++){
		if(b[i]==0){
			for(int j=i*2;j<10009;j=j+i){
				b[j]=1;
			}
		}
	}
	while(t--){
		int n;
		scanf("%d",&n);
		int k=0;
		int a[10001];
		for(int i=2;i<=n;i++){
			if(b[i]==0){
				a[k++]=i;
			}
		}
		for(int i=0;i<k;i++){
			for(int j=i;j<k;j++){
				if(a[i]+a[j]==n){
					printf("%d %d ",a[i],a[j]);
				}
			}
		}
		printf("\n");
	}
}
