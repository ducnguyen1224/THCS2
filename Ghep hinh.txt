#include<stdio.h>
#include<math.h>
int main(){
	int a[5],b[5];
	for(int i=1;i<=3;i++){
		scanf("%d %d",&a[i],&b[i]);
	}
	int x=0;
	for(int i=1;i<=3;i++){
		x+=a[i]*b[i];
	}
	int n=sqrt(x);
	if(n*n==x){
		int max1=0,max2=0;
		for(int i=1;i<=3;i++){
		if(a[i]>max1) max1=a[i];
	}
	for(int i=1;i<=3;i++){
		if(b[i]>max2) max2=b[i];
	}
	int max;
	if(max1>max2) max=max1;
	else max=max2;
	int c;
	int dem1=0;
	for(int i=1;i<=3;i++){
		if(a[i]==max) dem1++;
		if(b[i]==max) dem1++;
	}
	for(int i=1;i<=3;i++){
		if(a[i]==max) c=i;
		if(b[i]==max) c=i;
	}
	int q=abs(a[c]-b[c]);
	int dem=0;
	for(int i=1;i<=3;i++){
		if(a[i]==q||b[i]==q) dem++;
	}
	if(dem>=2||dem1==3) printf("YES");
	else printf("NO");
	}
	else printf("NO");
}