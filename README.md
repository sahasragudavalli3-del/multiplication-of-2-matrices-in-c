# multiplication-of-2-matrices-in-c
#include<stdio.h>
int main()
{
	int a[99][99],b[99][99],c[99][99];
	int i,j,k,r1,r2,c1,c2;
	scanf("%d %d",&r1,&c1);
	for(i=0;i<r1;i++)
		{
			for(j=0;j<c1;j++)
				{
					scanf("%d",&a[i][j]);
				}
		}
	scanf("%d %d",&r2,&c2);
	for(i=0;i<r2;i++)
		{
			for(j=0;j<c2;j++)
				{
					scanf("%d",&b[i][j]);
				}
		}
	if(c1==r2)
	{
		for(i=0;i<r1;i++)
			{
				for(j=0;j<c2;j++)
					{
						c[i][j]=0;
						for(k=0;k<r2;k++)
							{
							c[i][j]+=a[i][k]*b[k][j];
							
							}
						printf("%d ",c[i][j]);
					}
				printf("\n");
			}

	}
	else
	{
		printf("Not Possible");
	}
	return 0;
}
