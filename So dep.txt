#include<stdio.h>
#include<string.h>
int b[1000];
int  kt(char a[]){
	int l=strlen(a);
	for(int i=0;i<l;i++){
		a[i]=a[i]-48;
	}
	if(a[0]!=2*a[l-1] && a[0]*2!=a[l-1]) return 0;
	for(int i=1;i<l/2;i++){
		if(a[i]!=a[l-1-i]) return 0;
	}
	return 1;
}
main(){
	int t;
	scanf("%d",&t);
	while(t--){
		scanf("\n");
		char a[20];
		gets(a);
	    if(kt(a)==1) printf("YES");
	    else printf("NO");
		printf("\n");
		
		
		
		
	}
}
