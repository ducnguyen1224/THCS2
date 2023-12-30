#include<stdio.h>
#include<math.h>
int scp(long a){
	long x=sqrt(a);
	if(x*x==a) return 1;
	else return 0;
}
int main(){
	long a,b,i,d=0,m,n;
	scanf("%ld %ld",&a,&b);
	for(i=a;i<=b;i++){
		
		if(scp(i)==1){
		m=i; 
		break;
		}
	}
   for(i=b;i>=a+m;i--){
   	if(scp(i)==1) {
   		n=i;
   		break;
	   }
   }
   
   long x=sqrt(m),y=sqrt(n);
   printf("%ld\n",y-x+1);
   for(i=x;i<=y;i++){
   	long z=i*i;
   	printf("%ld\n",z);
   }
   
}
