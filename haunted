#include<stdio.h>
#include<stdlib.h>
 
	int age[100010];
	int c[100010];
	int a[100010];
	int b[100010];
 
int compare(int *a, int*b)
{
	return *a-*b;
}
 
int binarysearch(int n,int low,int high)
	{ int mid;
	  if (low > high)
	   return -1;
	  mid = (low + high)/2;
	  if(n == age[mid])
	    { 
	      return  mid;
	    }
	  if(n < age[mid])
	    { high = mid - 1;
	      return binarysearch(n,low,high);
	    }
	  if(n > age[mid])
	    { low = mid + 1;
	      return binarysearch(n,low,high);
	    }
	 }
 
/*
int fun(int x, int l, int h)
{
	int m = (h-l)/2;
	
	if(age[m] == x)
	return m;
	
	else if(age[m]<x)
	return fun(x, m+1, h);
	
	else return fun(x, l, m-1);
}
*/
 
int main()
{
	int  n, m, i, j, max[2];
	
	
	
	scanf("%d%d", &n, &m);
	
	for(i=0; i<n; i++)
	{
		scanf("%d", &a[i]);
		b[i]=a[i];
	}
	
	qsort(b, n, sizeof(int), compare);
	
	age[0]=b[0];
	j=1;
	
	for(i=1; i<n; i++)
	{
		if(b[i]!=age[j-1])
		{
			age[j]=b[i];
			j++;
		}
	}
	int M=j;
	
	for(i=0; i<M; i++)
	{
		//printf("%d ", age[i]);
		c[i]=0;
	}
	printf("\n");
	
	max[0]=-1;
	max[1]=-1;
 
	for(i=0; i<n; i++)
	{		
	
		
		int x = binarysearch(a[i], 0, M);
		//printf("debuging : %d\n", x);
		c[x]++;
		
		if(c[x]>max[0])
		{
			max[0]=c[x];
			max[1]=age[x];
		}
		else if(c[x]==max[0])
		{
			if(max[1]<age[x])
			max[1]=age[x];
		}
		
		printf("%d %d\n", max[1], max[0]);
	}	
	return 0; 	
}
