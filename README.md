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
    
## Ex04.c
 
    #include <stdio.h>
    #include <string.h>

    int main()
    {
    char str1[100], tmp;
    int l, lind, rind,i;

     printf("Enter a word : ");
     scanf("%s", str1);
     l = strlen(str1);

      lind = 0;
      rind = l-1;

      for(i=lind;i<rind;i++)
      {
     tmp = str1[i];
    str1[i] = str1[rind];
    str1[rind] = tmp;
     rind--;
    }

    printf("Inverted string is: %s\n\n", str1);
   }
   
       
## Ex04.py
 
    def string_reverse(str1):

    rstr1 = ''
    index = len(str1)
    while index > 0:
        rstr1 += str1[ index - 1 ]
        index = index - 1
    return rstr1
    print(string_reverse('djabd9u'))
    
 ## Ex05.c
  
    #include <stdio.h>
    int main() {
    int n, i;
    unsigned long long fact = 1;
    printf("Enter an integer: ");
    scanf("%d", &n);

    if (n < 0)
        printf("Invalid, it have to a positive integer");
    else {
        for (i = 1; i <= n; ++i) {
            fact *= i;
        }
        printf("Factorial of %d = %llu", n, fact);
    }

    return 0;
    }
    
## Ex05.py

    def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n-1)
    n=int(input("Input a number to compute the factiorial : "))
    print(factorial(n))
