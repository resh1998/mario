# mario

#include <stdio.h>
#include <cs50.h>

void pyramid(int n);

int main(void)

{
    // getting the height from the user
    printf("Height:");
    
    int higt = get_int();
    
    // making sure height is not negative
    if ( higt > 0 && higt < 24 )
    {
       
        // calling the function pyramid
        pyramid(higt);
    }
    
    
    // when height is negative or greater than 23 then print retry
    while(higt < 0 || higt > 23 )
    {
        printf(" Retry\n Height: ");
        scanf("%d", &higt);
        if ( higt > 0 && higt < 24 )
        {
       
            // calling the function pyramid
            pyramid(higt);
        }
    }
    
    
}

// defining the function pyramid
void pyramid(int n)

{
    
    // loop for printing space and #
    for(int i = 1; i <= n; i++)
    {
        for(int j = 1; j <= n - i; j++)
        {
            printf(" ");
        }
        
        for(int k = 1; k <= i + 1; k++)
        {
            printf("#");
        }
        
        printf("\n");
    }
}
