#include<stdio.h>
#include<math.h>
int nt(int a){
	if(a<2) return 0;
	else{
		for(int i=2;i<=sqrt(a);i++){
			if(a%i==0) return 0;
		}
		return 1;
	}
}
int ktsnt(int a){
	if(nt(a)==0) return 0;
	else{
		while(a>0){
			int d=a%10;
			if(nt(d)==0) return 0;
			a=a/10;
		}
		return 1;
	}
}
int main(){
	int t;
    scanf("%d",&t);
    while(t--){
    	int a,b;
    	int d=0;
    	scanf("%d %d",&a,&b);
    	for(int i=a;i<=b;i++){
    		if(ktsnt(i)==1) d++;
		}
		printf("%d",d);
		printf("\n");
}
}
