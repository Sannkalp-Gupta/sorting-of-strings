# sorting-of-strings
made it using sorting concepts and strings
#include<stdio.h>
#include<string.h>
int main()
{
	int n,i,j,t,flag;
	char city[10][20],swap[20];
	printf("Enter number of cities you want to sort=");
	scanf("%d",&n);
	printf("\nEnter %d cities name:\n",n);
	fflush(stdin);
	i=0;
	while(i<=n)
	{
		fgets(city[i],20,stdin);
		fflush(stdin);
		i++;
	}
	i=0;
	flag=0;
	while(i<=n-1)
	{
		j=0;
		while(j<=n-1-i)
		{
			if((strcmp(city[j],city[j+1]))>0)
			{
				strcpy(swap,city[j]);
				strcpy(city[j],city[j+1]);
				strcpy(city[j+1],swap);
				flag=1;
			}
			j++;
		}
		if(flag==0)
		{
			break;
		}
		i++;
	}
	i=0;
	printf("\n Cities in alphabetcal order are:");
	while(i<=n)
	{
		puts(city[i]);
		i++;
	}
	return 0;
}

