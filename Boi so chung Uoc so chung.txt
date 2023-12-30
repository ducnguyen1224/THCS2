#include<stdio.h>
#include<math.h>
int main(){
	int k,t;
	scanf("%d",&t);
	for(k=0;k<t;k++){
		long long a,b,LCM;
		scanf("%lld %lld",&a,&b);
		long long d,GCD=b,m=a;
		while(a%GCD!=0){
			d=a%GCD;
			a=GCD;
			GCD=d;
		}
		LCM=m*b/GCD;
		printf("%lld %lld",LCM,GCD);
		printf("\n");
	}
	return 0;
		
}
