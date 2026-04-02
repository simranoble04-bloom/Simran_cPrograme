# Simran_cPrograme

# include <stdio.h>
# include <math.h>

struct train_info {
    int train_no;
    char name[20];
    float dep_time;
    float arr_time;
    char start_st[30];
    char end_st[30];
};

int main() {

    /* Q1. WAP that accepts the marksd of 5 subjects and finds the sum and percentage of marks obtained by student*/
    float mm1, mm2, mm3, mm4, mm5, sum, per;
    printf("enter mm1, mm2, mm3, mm4, mm5: ");
    scanf("%f %f %f %f %f", &mm1, &mm2, &mm3, &mm4, &mm5);
    sum = mm1+mm2+mm3+mm4+mm5;
    per = (sum/500)*100;
    printf("Sum of maks = %f and, percentage = %f", sum, per);

    /* Q5. WAP to swap two numbers and and b*/

    /* using 3rd var*/
    int a, b, temp;
    printf("enter a and b :");
    scanf("%d %d", &a, &b);
    temp=a;
    a = b;
    b = temp;
    printf("new val of a = %d and b= %d\n", a, b);

    /*using only entered two nums*/
    int num1, num2;
    printf("enter num1 and num2 :");
    scanf("%d %d", &num1, &num2);
    num1 = num1 + num2;
    num2 = num1 - num2;
    num1 = num1 - num2;
    printf("new val of num1 = %d and num2 = %d\n", num1, num2);

    /* Q6. WAP that checks weather the num entered by user is equal or not*/
    int n1, n2;
    printf("enter n1 and n2: ");
    scanf("%d %d", &n1, &n2);
    if (n1==n2) {
        printf("Yes!, n1 and n2 are equal");
    }
    else {
        printf("No!, n1 and n2 are not equal");
    }

    /* Q7. WAP to find the greatest of three numbers*/
    int a1, a2, a3;
    printf("enter a1, a2 and a3: ");
    scanf("%d %d %d", &a1, &a2, &a3);
    if (a1>a2 && a1>a3) {
        printf("a1 is the greatest: %d", a1);
    }
    else if (a2>a1 && a2>a3) {
        printf("a2 is the greatest: %d", a2);
    }
    else {
        printf("a3 is greatest: %d", a3);
    }

    /* Q8. WAP that finds weather a given num is odd or even*/
    int b1;
    printf("enter b1: ");
    scanf("%d", &b1);
    if (b1%2==0) {
        printf("b1 is even");
    }
    else {
        printf("b1 is odd");
    }

    /* Q9. WAP that tells weather a given year is leap year or not */
    int y;
    printf("enter year y: ");
    scanf("%d", &y);
    if (y%4==0 && y%100!=0) {
        if (y%400==0) {
    } printf("Yes!, it's a leap year : %d\n", y);
    }
    else {
        printf("No!, it's not a leap year : %d\n", y);
    }

    /* Q10. WAP that accepts marks of five subj and finds percentage and prints grades accordingly :
            90-100% (print A)
            80-90% (print B) 
            60-80% (print C)
            below 60% (print D)*/
    float m1, m2, m3, m4, m5, percentage;
    printf("enter marks of 5 subjects out of 100: ");
    scanf("%f %f %f %f %f", &m1, &m2, &m3, &m4, &m5);
    percentage = ((m1+m2+m3+m4+m5)/500)*100;
    
    if (percentage>90 && percentage<=100) {
        printf("your percentage = %f and your grades = A\n", percentage);
    }
    else if (percentage>80 && percentage<=90) {
        printf("your percentage = %f and your grades = B\n", percentage);
    }
    else if (percentage>60 && percentage<=80) {
        printf("your percentage = %f and your grades = C\n", percentage);
    }
    else {
        printf("your percentage = %f and your grades = D\n", percentage);
    }

    /* Q11. WAP that takes two operands and one operator from the user and 
    performs the operation and print the result by using switch statement*/
    float oprnd1, oprnd2, result;
    char oprtr;
    printf("enter operand1: ");
    scanf("%f", &oprnd1);
    printf("enter operand2: ");
    scanf("%f", &oprnd2);
    printf("enter the operator: ");
    scanf(" %c", &oprtr);

    switch (oprtr) {
        case '+' :
            result = oprnd1+oprnd2;
            printf("oprnd1+oprnd2 = %f", result);
            break;
        case '-' :
            result = oprnd1-oprnd2;
            printf("oprnd1-oprnd2 =%f", result);
            break;
        case '*' :
            result = oprnd1*oprnd2;
            printf("oprnd1*oprnd2 =%f", result);
            break;
        case '/' :
            if (oprnd2==0) {
                printf("oprnd2 cannot be zero");
            }
            else {
                result = oprnd1/oprnd2;
            printf("oprnd1/oprnd2 =%f", result);
            }
            break;
        default :
            printf("operator not defined");
            break;
}

/* Q12. Wap to print the sum of all numbers upto a given number. */

int nn, sm=0; 
printf("enter number nn: ");
scanf("%d", &nn);

for(int i=nn; i>0; i--) {
    sm = sm+i;
}

/* Q13. WAP to print the factorial of a given number*/

int fn, fact=1;
printf("enter number fn: ");
scanf("%d", &fn);

for(int i=fn; i>0; i--) {
    fact*=i;
}
printf("Factorial is : %d\n*", fact);

/*Q14. WAP to print the sum of odd and even numbers from 1 to N numbers. */

int nms, sum_O=0, sum_E=0;
printf("enter number nms: ");
scanf("%d", &nms);

for(int i=nms; i>0; i--) {
    if(i%2==0) {
        sum_E+=i;
    }
    else {
        sum_O+=i;
    }
}
printf("sum of even numbers = %d, sum of odd numbers = %d\n", sum_E, sum_O);

/* Q15. WAP to print the fibonacci series. */

int terms, f_n=0, s_n=1, N;
printf("enter number terms: ");
scanf("%d", &terms);

while(terms>0) {
    N = f_n+s_n;
    f_n=s_n;
    s_n=N; 
    terms--;
    printf("The fibonacci series is : %d\n", N);
}

/*Q16. WAP to check weather the entered number is prime or not. */

int p_n, is_prime=1;
printf("enter a number to check if it's prime or not as p_n: ");
scanf("%d", &p_n);

if(p_n<2) {
    is_prime=0;
}
else {
    for(int i=p_n/2; i>0; i--) {
        if (p_n%i==0) {
            is_prime=0;
            break;
        }
        else {
            is_prime=1;
        }
    }
}
if(is_prime) {
    printf("Yes, %d is a prime number", p_n);
}
else {
    printf("No, %d is not a prime number", p_n);
}

/*Q17. WAP to print the sum of digits of a given number.*/
int Nm, dg, dg_sum=0, org_Nm;
printf("Enter Number Nm: ");
scanf("%d", &Nm);
org_Nm=Nm;

while(Nm>0) {
    dg=Nm%10;
    dg_sum+=dg;
    Nm/=10;
}
printf("The sum of digits of %d is= %d\n", org_Nm, dg_sum);

/*Q18. WAP to find the reverse of a number. */
int Num, dig, rev=0, org_Num;
printf("Enter Number Num: ");
scanf("%d", &Num);
org_Num = Num;

while(Num>0) {
    dig = Num%10;
    rev = rev*10 + dig;
    Num/=10;
}
printf("The reverse of %d is = %d\n", org_Num, rev);

/*Q19. WAP to print the armstrong numbers from 1 to 100. */
int NuM, dd=0, org_NuM, nn, Arm_sum=0;
printf("enter number NuM: ");
scanf("%d", &NuM);
org_NuM = NuM;

while(NuM>0) {
    dd+=1;
    NuM/=10;
}
printf("%d\n", dd);
NuM= org_NuM;

while(NuM>0){
    nn=NuM%10;
    Arm_sum += pow(nn, dd);
    NuM/=10;
}
if(org_NuM==Arm_sum) {
    printf("Yes, %d is an armstrong number", NuM);
}
else {
    printf("No, it's not an armstrong");
}

/* WAP to convert binary number into decimal number and vice versa. */

/* Q. WAP to find the roots of a quadratic equation.*/
int A1, B1, C1;
float D1;
double R1, R2;
printf("Enter A1, B1, C1: ");
scanf("%d %d %d", &A1, &B1, &C1);

D1 = B1*B1 - 4*A1*C1;

if(D1>0) {
    R1=(-B1 + sqrt(D1))/2*A1;
    R1=(-B1 + sqrt(D1))/2*A1;
    printf("The roots are :-\n Root1 = %1f and Root2 = %1f", R1, R2);

}
else {
    if(D1==0) {
        R1 = (-B1*B1)/(2*A1);
        R1=R2;
        printf("The roots are :-\n Root1 = %1f and Root2 = %1f", R1, R2);

    }
    else {
        printf("Roots are imaginary");
    }
}

/* WAP to print a square pattern */
int sq_n;
printf("Enter the dimensions of square sq_n: ");
scanf("%d", &sq_n);

for(int i=1; i<=sq_n; i++) {
    for(int j=1; j<=sq_n; j++) {
        printf("* ");
    }
    printf("\n");
}

/* Q. WAP to print a triangle. */
int tr_h; 
printf("Enter the dimensions of triangle tr_h : ");
scanf("%d", &tr_h);

for(int i=1; i<=tr_h; i++) {
    for(int j=1; j<=i; j++) {
        printf("* ");
    }
    printf("\n");
}
printf("\n");


for(int i=1; i<=tr_h; i++) {
    for(int j=1; j<=(tr_h-i); j++) {
        printf("  ");
    }
    for(int k=1; k<=i; k++) {
        printf("* ");
    }
    printf("\n");
}

    int a[50], n, sum=0;
    printf("Enter n: ");
    scanf("%d", &n);

    for(int i=0; i<n; i++){
        printf("Enter a[%d]: ", i);
        scanf("%d", &a[i]);
    }
    for(int i=0; i<n; i++){
        printf("%d\t", a[i]);
    }
    printf("\n");

    /*Q. WAP to print the sum of elements of an array. */

    for(int i=0; i<n; i++){
        sum+=a[i];
    }
    printf("Sum of elements of array a = %d\n", sum);

    /*Q. WAP to print the max and min among elements of an array. */

    int max=a[0], min=a[0], t;

    for(int i=1; i<n; i++){
        if(max<a[i]){
            t=max;
            max=a[i];
            a[i]=t;
        }
    }
    printf("max elements of array a = %d\n", max);
    for(int i=1; i<n; i++){
        if(min>a[i]){
            t=min;
            min=a[i];
            a[i]=t;
        }
    }
    printf("min elements of array a = %d\n", min);

    /*WAP that inputs two arrays and prints the sum of corresponding elemenys to some another array. */
    int b[50], c[50], n1, n2, bc[100], n3, sum=0, temp;
    printf("Enter elements of array b: ");
    scanf("%d", &n1);
    printf("Enter elements of array c: ");
    scanf("%d", &n2);
    printf("Enter elements of array c: ");

    scanf("%d", &n3);

    for(int i=0; i<n1; i++){
        printf("Enter b[%d]: ", i);
        scanf("%d", &b[i]);
    }
    for(int i=0; i<n2; i++){
        printf("Enter c[%d]: ", i);
        scanf("%d", &c[i]);
    }
    if(n1>n2){
        temp=n1;
    }
    else{
        temp=n2;
    }
    for(int i=0,j=0; i<temp,j<temp; i++,j++){
        bc[i]=b[i]+c[i];
        printf("%d\t", bc[i]);
    }

    /*WAP to search an element in an array using linear search*/
    int a[50], n, key, t;
    printf("Enter element n: ");
    scanf("%d", &n);

    for(int i=0; i<n; i++){
        printf("Enter a[%d]: ", i);
        scanf("%d", &a[i]);
    }

    printf("Enter key: ");
    scanf("%d", &key);

    for(int i=0; i<n; i++){
        if(key==a[i]){
            printf("Element %d found at index: %d\n", key, i);
        }
    }

    /*WAP to sort elements of an array in increasing order - Using bubble sort*/
    for(int i=0; i<n; i++){
        for(int j=0; j<n-1-i; j++){
            if(a[j]>a[j+1]){
                t=a[j];
                a[j]=a[j+1];
                a[j+1]=t;
            }
        }
    }
    for(int i=0; i<n; i++){
        printf("%d\t ", a[i]);
    }


/* WAP to create a 2D array and perform the multiplication. */
    int a[50][50], b[50][50], c[50][50], r1, c1, r2, c2;
    printf("Enter no of rows and column of a: ");
    scanf("%d %d", &r1, &c1);

    printf("Enter number of rows and column of b: ");
    scanf("%d %d", &r2, &c2);

    for(int i=0; i<r1; i++){
        for(int j=0; j<c1; j++){
            printf("Enter a[%d][%d]: ", i, j);
            scanf("%d", &a[i][j]);
        }
    }
    
    for(int i=0; i<r2; i++){
        for(int j=0; j<c2; j++){
            printf("Enter b[%d][%d]: ", i, j);
            scanf("%d", &b[i][j]);
        }
    }
    
    for(int i=0; i<r1; i++){
        for(int j=0; j<c1; j++){
            printf("%d\t", a[i][j]);
        }
        printf("\n");
    }
    printf("\n");
    
    for(int i=0; i<r2; i++){
        for(int j=0; j<c2; j++){
            printf("%d\t", b[i][j]);
        }
        printf("\n");
    }
    printf("\n");

    /*Multiplication */
    if(c1==r2){
        for(int i=0; i<r1; i++){
            for(int j=0; j<c2; j++){
                for(int k=0; k<r2; k++){
                    c[i][j]+=a[i][k]*b[k][j];
                }
            }
        }
        printf("\nProduct of the matrices:\n");
        for (int i = 0; i < r1; i++) {
            for (int j = 0; j < c2; j++) {
                printf("%d\t", c[i][j]);
            }
            printf("\n");
        }
    }
      
/* WAP to arrange elements of an array using insertion sort technique*/
#include <stdio.h>

void insertion(int a[], int n){
    int i, j, temp;
    for(i=1; i<n; i++){
        temp = a[i];
        j=i-1;
        while(j>=0 && temp < a[j]){
            a[j+1] = a[j];
            j--;
        }
        a[j+1]=temp;
    }
}

void print(int a[], int n) {
    int i;
    for(i=0; i<n; i++){
        printf("%d\t", a[i]);
    }
    
}

int main(){
    int a[50], n, i;
    printf("Enter number of elements: ");
    scanf("%d", &n);
    for(i=0; i<n; i++){
        printf("Enter a[%d]: ", i);
        scanf("%d", &a[i]);
    }
    printf("Array before sorting...\n");
    print(a, n);
    insertion(a, n);
    printf("Array After sorting...\n");
    print(a, n);

    return 0;
}

/* WAP to sort elements of an array using selection sort. */
#include <stdio.h>

void selection(int a[], int n){
    int i, j, min, temp;
    for(i=0; i<n-1; i++){
        min = i;
        for(j=i+1; j<n; j++){
            if(a[j]<a[min]){
                min=j;
            }
            if(min!=i){
                temp=a[i];
                a[i]=a[min];
                a[min]=temp;
            }
        }
    }
}

void print(int a[], int n) {
    int i;
    for(i=0; i<n; i++){
        printf("%d\t", a[i]);
    }
    
}

int main(){
    int a[50], n, i;
    printf("Enter number of elements: ");
    scanf("%d", &n);
    for(i=0; i<n; i++){
        printf("Enter a[%d]: ", i);
        scanf("%d", &a[i]);
    }
    printf("Array before sorting...\n");
    print(a, n);
    selection(a, n);
    printf("Array After sorting...\n");
    print(a, n);

    return 0;
}









    return 0;
}

