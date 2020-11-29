# balanced-parathesis
To find number of balanced parathesis without using stack
#include <stdio.h>
#include<string.h>
int main() {
    char a[20];
    int len=0,o=0,c=0,i=0,result=0;
    printf("Enter the string: ");
    gets(a);
    len=strlen(a);
    for(i=0;i<len;i++)
    {
        if(a[i]=='(')
        {
            if(a[i+1]==')')
            {
                o=o+1;
                c=c+1;
                i=i+1;
                continue;
            }
        }
         if(a[i]==')')
        {
            if(a[i+1]=='(')
            {
                o=o+1;
                c=c+1;
                i=i+1;
            }
        }
       
    }
    result=o+c;
    printf("The result is %d",result);
    
    return 0;
}
