#include<stdio.h>
#include<math.h>
int main(){
	int t,k;
	scanf("%d",&t);
	for(k=0;k<t;k++){
	long n,d=0,i;
	scanf("%ld",&n);
	
	for(i=1;i<=sqrt(n);i++){
		if(n%i==0 ){
          if(i%2==0) d++;
      if((n/i)%2==0 && i*i!=n) d++;
    
	}
}
	printf("%ld\n",d);

}
}
