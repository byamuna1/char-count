
// Sample code to perform I/O:

#include <iostream>

using namespace std;

int main() {
	int t;
	cin>>t;
	char s[t];
    int a[26]={0},b[26]={0},aa[t]={0},bb[t]={0},n,i;
	cin>>s;
	for( i=0;s[i]!='\0';i++)
	{
	    int x=s[i]-97;
	    a[x]=a[x]+1;
	}
	for(i=0;s[i]!='\0';i++)
	{
	    int c=s[i]-97;
	     aa[i]=b[c];
	     b[c]=b[c]+1;
	     a[c]=a[c]-1;
	     bb[i]=a[c];
	}

	int q;
	cin>>q;
	for(i=0;i<q;i++)
	{
	    cin>>n;
	    cout<<aa[n-1]<<" "<<bb[n-1]<<endl;
	}

}
