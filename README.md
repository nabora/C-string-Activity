#include <stdio.h>
#include <string.h>
int main()
{
    char string1[200];
    int  i, vowels = 0, consonants = 0;
   printf("Input a sentence: ");
   fgets(string1, 200, stdin);
   i=0;
    while(string1[i]!='\0')
    {
        if(string1[i]=='a' ||string1[i]=='e' ||string1[i]=='i' ||string1[i]=='o' ||string1[i]=='u')
            string1[i]=string1[i]-32;
        i++;
    }
    printf("String converted: ");
    puts(string1);

    // using the %zu format specifier to print size_t
    
    printf("\nString lenght: %zu \n", strlen(string1));
    
       for(i=0;string1[i];i++)  
    
    	if((string1[i]>=65 && string1[i]<=90)|| (string1[i]>=97 && string1[i]<=122))
    	{
		
            if(string1[i]=='a'|| string1[i]=='e'||string1[i]=='i'||string1[i]=='o'||string1[i]=='u'||string1[i]=='A'||string1[i]=='E'||string1[i]=='I'||string1[i]=='O' ||string1[i]=='U')
		      vowels++;
            else
             consonants++;
        }
 
    printf("vowels: %d\n",vowels);
    printf("consonants: %d\n",consonants);
    }
    
