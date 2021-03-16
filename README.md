## Ex01.c

    #include <stdio.h>
    int main() {
      double n1, n2, n3;
      printf("Enter three different numbers: ");
      scanf("%lf %lf %lf", &n1, &n2, &n3);

      if (n1 >= n2 && n1 >= n3)
      printf("%.2f is the largest number.", n1);
        if (n2 >= n1 && n2 >= n3)
        printf("%.2f is the largest number.", n2);
             if (n3 >= n1 && n3 >= n2)
             printf("%.2f is the largest number.", n3);

    return 0;
    }
 
 ## Ex01.py
 
    def max_of_two( x, y ):
     if x > y:
        return x
     return y
    def max_of_three( x, y, z ):
     return max_of_two( x, max_of_two( y, z ) )
    print(max_of_three(1, 2, 3))
    
 ## Ex02.c
 
     #include <stdio.h>
     
    int main()
    {
    int a[1000],i,n,sum=0;
   
    printf("Enter size of the array : ");
    scanf("%d",&n);
 
    printf("Enter elements in array : ");
    for(i=0; i<n; i++)
    {
        scanf("%d",&a[i]);
    }
    for(i=0; i<n; i++)
    { 
        sum+=a[i];
    }
     printf("sum of array is : %d",sum);
 
    return 0;
    }

## Ex02.py

    def sum(numbers):
    total = 0
    for x in numbers:
        total += x
    return total
    print(sum((5, -2, 4, 6, 2, 4)))
    
 ## Ex03.c
 
    #include <stdio.h>

    char line[100];
    int n1; 
    int n2; 
    int m; 
    int main()
    {
    printf("Enter 2 numbers ");
    fgets(line, sizeof(line), stdin);
    sscanf(line, "%d %d", &n1, &n2);
    sscanf(line, "%d %d", &n1, &n2);
     m = (n1 * n2);
     printf("The multiplication of the numbers is %d\n", m);
    return (0);
    }
     
 ## Ex03.py
 
    def multiply(numbers):  
     total = 1
    for x in numbers:
        total *= x  
    return total  
    print(multiply((4, 5, 2, 4)))
