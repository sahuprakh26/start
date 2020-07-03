#include<stdio.h>
#include<string.h>

int main()
{
	int x,y,i;
	char orient;
	char mp[20];
	printf("Starting position:");
	scanf("%d %d %c",&x, &y, &orient);
    printf("Movement Plan:");
    scanf("%s",&mp);
    for(i=0;i<strlen(mp);i++)
    {
    	if (mp[i]=='L')
         {
         	if(orient=='N')
         	orient='W';
         	
         	else if(orient=='W')
             orient='S';
 
             else if(orient=='S')
              orient='E';
 
            else if(orient=='E')
             orient='N';

		 }    	
		 if(mp[i]=='R')
		 {
		 if(orient=='N')
          orient= 'E'; 
 
         else if(orient=='E')
           orient='S';
 
        else if(orient=='S')
         orient='W';
 
        else if(orient=='W')
         orient='N';
         }
         
         if(mp[i]=='M')
         {
         	if(orient=='N')
         	 y++;
         	 else if (orient=='S')
         	 y--;
         	 else if(orient=='E')
         	 x++;
         	 else if(orient=='W')
         	 x--;
		 }
		 
		 
	}
	printf("Final Position: %d %d %c",x,y,orient);
	return 0;
	
	
}
