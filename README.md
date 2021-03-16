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
    
## Ex06.c

    #include<stdio.h>
 
    int main() {
    int num, min, max;
     
    printf("Enter an integer\n");
    scanf("%d", &num);
    printf("Enter the minimum and maximum range\n");
    scanf("%d %d", &min, &max);
     
    if((num-min)*(num-max) <= 0){
        printf("%d is in range of [%d, %d]", num, min, max);
    } else {
     printf("%d is not in range of [%d, %d]", num, min, max);
    }
    return 0;
   }
   
## Ex06.py
 
    def test_range(n):
    if n in range(6,12):
        print( " %s is in the range"%str(n))
    else :
        print("The number is outside the given range.")
    test_range(8)
  
 ## Ex07.c

    #include <stdio.h>
    #include <stdlib.h>
    int main()
    {
    int i;
    int upper=0,lower=0;
    char ch[100];
    printf("Enter the String:\n");
    gets(ch);
    for(i=0; ch[i]!=0; i++){
      if(ch[i]>='A' && ch[i]<='Z'){
       upper++;
     }
      else if(ch[i]>='a' && ch[i]<='z'){
      lower++;
     }
     }
    printf("lowercase letters: %d",lower);
    printf("\nuppercase letters: %d",upper);

    return 0;
    }
    
## Ex07.py

    def string_test(s):
    d={"UPPER_CASE":0, "LOWER_CASE":0}
    for c in s:
        if c.isupper():
           d["UPPER_CASE"]+=1
        elif c.islower():
           d["LOWER_CASE"]+=1
        else:
           pass
    print ("Original String : ", s)
    print ("No. of Upper case characters : ", d["UPPER_CASE"])
    print ("No. of Lower case Characters : ", d["LOWER_CASE"])

    string_test('I Have Many HW')
  
## Ex08.c

    #include <stdio.h>
    int main()
    {
    int arr1[100], n,ctr=0;
    int i, j, k;
       	
       printf("Input the number of elements to be stored in the array: ");
       scanf("%d",&n);
       printf("Input %d elements in the array :\n",n);
       for(i=0;i<n;i++)
            {
	      printf("element - %d : ",i);
	      scanf("%d",&arr1[i]);
	    }
    printf("\nThe unique elements found in the array are: \n");
    for(i=0; i<n; i++)
    {
        ctr=0;
        for(j=0,k=n; j<k+1; j++)
        {
      
            if (i!=j)
            {
		       if(arr1[i]==arr1[j])
              {
                 ctr++;
               }
             }
        }
       if(ctr==0)
        {
          printf("%d ",arr1[i]);
        }
    }
       printf("\n\n");
    }
    
## Ex08.py

    def unique_list(l):
    x = []
    for a in l:
    if a not in x:
      x.append(a)
    return x

    print(unique_list([1, 2, 3, 4, 5, 5, 14])) 
    
 ## Ex09.c
 
     #include <stdio.h>
     int main() {
      int n, i, flag = 0;
      printf("Enter a positive integer: ");
      scanf("%d", &n);

      for (i = 2; i <= n / 2; ++i) {
      if (n % i == 0) {
      flag = 1;
      break;
     }
     }

    if (n == 1) {
    printf("1 is neither prime nor composite.");
  } 
         else {
           if (flag == 0)
        printf("%d is a prime number.", n);
            else
      printf("%d is not a prime number.", n);
    }

     return 0;
     }
 ## Ex09.py

  
