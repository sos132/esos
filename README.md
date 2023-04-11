All Programs.

/*Write a java program that takes a number as input and prints the multiplication table upto 10*/

import java.util.Scanner;
class RPrac1a{
public static void main(String args[])
{
int num, i;
Scanner st = new Scanner(System.in);
System.out.println("Enter number: ");
num = st.nextInt();
System.out.println("Table of"+num);
for(i=1;i<=10;i++)
{
System.out.println(num+"*"+i+"="+num*i);
}
}
}

/*Write a java program to display the following pattern 
*****
****
***
**
*
The above pattern👆*/

import java.util.Scanner;
class RPrac1b{
public static void main(String args[])
{
int i,j;
for(i=5;i>=1;i--)
{
for(j=1;j<=i;j++)
{
System.out.print('*');
}
System.out.println();
}
}
}

/*Write a java program to print the area and perimeter of a circle*/

import java.util.scanner;
class RPrac1c{
public static void main(String args[])
{
double r,cp,ca; //dble coz pi
Scanner st = new Scanner(System.in);
System.out.println("Enter radius of a cirlce: ");
r = st.nextDouble();
cp = 2*3.14*r;
ca = 2*r*r;
System.out.println("Perimeter= "+cp);
System.out.println("Area= "+ca);
}}

/*Write a Java program to add two binary numbers.*/
  
import java.util.Scanner;
class Pract2a
{
public static void main(String args[])
{
long b1,b2;
int i=0,rem=0;
int[] sum=new int[20];
Scanner in =new Scanner(System.in);
System.out.print("Enter first binary number:-");
b1=in.nextLong();
System.out.print("Enter second binary number:-");
b2=in.nextLong();
while(b1!=0||b2!=0)
{
sum[i++]=(int)((b1%10+b2%10+rem)%2);
rem=(int)((b1%10+b2%10+rem)/2);
b1=b1/10;
b2=b2/10;
}
if(rem!=0)
{
sum[i++]=rem;
}
--i;
System.out.print("Sum of b1+b2= ");
while(i>=0)
{
System.out.print(sum[i--]);
}
}
}

/*Write a java program to convert a decimal number to binary number and vice versa*/

import java.util.Scanner;
class RPrac2b
{
public static void main(String args[])
{
String num1; // remember num1 should be String
int num2; // remember num2 should be int
Scanner in = new Scanner(System.in);
System.out.print("Enter binary number: ");
num1=in.nextLine(); //In string nextLine is used
System.out.println("Enter decimal number: ");
num2 = in.nextInt();
System.out.println("Binary to Decimal: "+Integer.parseInt(num1,2)); //parseInt is used to convert binary to decimal
System.out.println("Decimal to Binary: "+Integer.toBinaryString(num2)); //toBinaryString is used to convert decimal to binary
// remember to add Integer. before parseInt and toBinaryString(these 2 methods)
}
}

/*Write a java program to reverse a string*/

import java.util.Scanner;
class RPrac2c{
public static void main(String args[])
string s,t="";
int len,i;
Scanner  in = new Scanner(System.in)
System.out.print("Enter a string: ");
s = in.nextLine;
len = s.length();
for(i=len-1;i>=0;i--);
t=t+s.charAt(i);
System.out.println("Reverse: "+t);
}}

/*Write a Java program to count the letters, spaces, numbers, and other characters of an input string.*/

import java.util.Scanner;
class Pract3a
{
public static void main(String args[])
{
String st;
Scanner in =new Scanner(System.in);
System.out.print("Enter a string:-");
st=in.nextLine();
count(st);
}
public static void count(String x)
{
char[] ch=x.toCharArray();
int i,l=0,s=0,d=0,a=0;
for(i=0;i<x.length();i++)
{
if(Character.isLetter(ch[i]))
{
l++;
}
else if(Character.isDigit(ch[i]))
{
d++;
}
else if(Character.isSpaceChar(ch[i]))
{
s++;
}
else
{
a++;
}
}
System.out.println("Letter:-"+l);
System.out.println("Space:-"+s);
System.out.println("Number:-"+d);
System.out.println("Other:-"+a);
} }

/*Implement a Java function that calculates the sum of digits for a given char array consisting of the digits '0' to '9'. The function should return the digit sum as a long value.*/

import java.util.Scanner;
class RPrac3b
{
public static long calc()
{
int i;
long x=0L,sum=0L;
char c[]={'0','1','2','3','4','5','6','7','8','9'};
for(i=c.length-1;i>=0;i--)
{
x=c[i]-'0';
sum=sum+x;
}
return sum;
}
public static void main(String args[])
{
long s=calc();
System.out.print("Sum is "+s);
}
}

/*Find the smallest and largest element from the array*/

import java.util.Scanner;
class Pract3c
{
public static void main(String args[])
{
int num[]=new int[]{13,22,27,11,4};
int s=num[0];
int l=num[0];
int i; 
System.out.println("Array Elements are:-");
for(i=0;i<num.length-1;i++)
{
System.out.println(num[i]);
}
for(i=1;i<num.length-1;i++)
{
if(num[i]>l)
l=num[i];
else if(num[i]<s)
s=num[i];
}
System.out.println("Largest Number in array:-"+l);
System.out.println("Smallest Number in array:-"+s);
}
}

/*Designed a class SortData that contains the method asec() and desc().*/
 
class SortData {
 int n,temp,i,j;
 public void asec(int num[]) {
 for (int i = 0; i < num.length; i++) {
 for (int j = i+1; j < num.length ; j++) {
 if(num[i]>num[j]) {
 temp= num[i];
 num[i]=num[j];
 num[j]=temp;
 }
 }
 }
 System.out.println("Assending Order");
 for (int i = 0; i < num.length ; i++) {
 System.out.println(num[i]+" ");
 }
}
 public void desc(int num[]) {
 for (int i = 0; i < num.length; i++) {
 for (int j = i+1; j < num.length ; j++) {
 if(num[i]<num[j])
 {
 temp= num[i];
 num[i]=num[j];
 num[j]=temp;
 }
 }
 }
 System.out.println("Descending Order");
 for (int i = 0; i < num.length ; i++) {
 System.out.println(num[i]+" ");
 }
 }
}
public class Prac4a {
 public static void main(String[] args) {
 SortData obj=new SortData();
 int arr[]={13,22,27,11,4};
 obj.asec(arr);
 obj.desc(arr);
 }
}

/*Designed a class that demonstrates the use of constructor and destructor.*/

public class Prac4b
 {
    public Prac4b()
    {
    System.out.println("Hello");
    }
    public void Finalize()
    {
    System.out.println("Destroyed");
    }	
    public static void main(String[] args) {
    Prac4b obj=new Prac4b();
    obj=null;
    System.gc();
    }
}

/*Write a java program to demonstrate the implementation of abstract class.*/ 

abstract class Calc {
 public abstract int sqr(int n1);
 public abstract int cube(int n1);
 public void show()
 {
 System.out.println("Hello");
 }
}
public class Prac4c extends Calc
{
 @Override
 public int sqr(int n1) {
 return n1*n1;
 }
 @Override
 public int cube(int n1) {
 return n1*n1*n1; 
 }
 public static void main(String[] args) {
 Prac4c obj=new Prac4c();
 int sq= obj.sqr(4);
 System.out.println("4's Square= "+sq);
 int cube= obj.cube(4);
 System.out.println("4's Cube= "+cube);
 }
}

/*Write a java program to implement single level inheritance*/

class Demo {
float pi=3.142f; 
 void show()
 {
 System.out.println("Area of circle");
 }
}
public class Prac5a extends Demo
{
 float r=2.0f;
 void area()
 {
 System.out.println(pi*r*r);
 }
 public static void main(String[] args) {
 Prac5a obj=new Prac5a();
 obj.show();
 obj.area();
 }
}

/*Write a java program to implement method overriding*/ 

class A {
 void show()
 {
 System.out.println("Base Class");
 }
}
class B extends A
{
 void show()
 {
 System.out.println("Derived Class");
 } 
}
public class Prac5b {
 public static void main(String[] args) {
 B ob=new B();
 ob.show();
 }
}

/*Write a java program to implement multiple inheritance.*/ 

interface S {
 public void show();
}
 interface T extends S
{
 public void display();
}
public class Prac5c implements T
{
 @Override
 public void display() {
 System.out.println("From Interface T");
 }
 @Override
 public void show() {
 System.out.println("From Interface S");
 }
 public static void main(String[] args) {
 Prac5c ob=new Prac5c();
 ob.show();
 ob.display();
 }
}

/*Write a java program to add two matrices and print the resultant matrix.*/

import java.util.Scanner;
public class MatAdd
{
 public static void main(String args[])
 {
 int i, j;
 int mat1[][] = new int[2][2];
 int mat2[][] = new int[2][2];
 int mat3[][] = new int[2][2];
 Scanner scan = new Scanner(System.in);
 
 System.out.print("Enter Matrix 1 Elements : ");
 for(i=0; i<2; i++)
 {
 for(j=0; j<2; j++)
 {
 mat1[i][j] = scan.nextInt();
 }
 }
 System.out.print("Enter Matrix 2 Elements : ");
 for(i=0; i<2; i++)
 {
 for(j=0; j<2; j++)
 {
 mat2[i][j] = scan.nextInt();
 }
 }
 System.out.print("Adding both Matrix to form the Third Matrix...\n");
 for(i=0; i<2; i++)
 {
 for(j=0; j<2; j++)
 {
 mat3[i][j] = mat1[i][j] + mat2[i][j];
 }
 }
 System.out.print("The Two Matrix Added Successfully..!!\n");
 System.out.print("The New Matrix will be :\n");
 for(i=0; i<2; i++)
 {
 for(j=0; j<2; j++)
 {
 System.out.print(mat3[i][j]+ " ");
 }
 System.out.println();
 }
 }
}

/*Write a java program to add two matrices and print the resultant matrix.*/

import java.util.Scanner;
public class MatrixMultiply
{
 public static void main(String args[])
 {
 int n;
 Scanner input = new Scanner(System.in);
 System.out.println("Enter the base of squared matrices");
 n = input.nextInt();
 int[][] a = new int[n][n];
 int[][] b = new int[n][n];
 int[][] c = new int[n][n];
 System.out.println("Enter the elements of 1st martix row wise \n");
 for (int i = 0; i < n; i++)
 {
 for (int j = 0; j < n; j++)
 {
 a[i][j] = input.nextInt();
 }
 }
 System.out.println("Enter the elements of 2nd martix row wise \n");
 for (int i = 0; i < n; i++)
 {
 for (int j = 0; j < n; j++)
 {
 b[i][j] = input.nextInt();
 }
 }
 System.out.println("Multiplying the matrices...");
 for (int i = 0; i < n; i++)
 {
 for (int j = 0; j < n; j++)
 {
 for (int k = 0; k < n; k++)
 {
 c[i][j] = c[i][j] + a[i][k] * b[k][j];
 }
 }
 }
 System.out.println("The product is:");
 for (int i = 0; i < n; i++)
 {
 for (int j = 0; j < n; j++)
 {
 System.out.print(c[i][j] + " ");
 }
 System.out.println();
 }
 }
}

/*Write a java program to implement the vectors.*/

import java.util.Vector;
class Pract7a
{
public static void main(String args[])
{
Vector<String> v=new Vector<String>();
v.add("Red");
v.add("Green");
v.add("Blue");
System.out.println("Vector Elements are:-"+v);
v.add(2,"Yellow");
System.out.println("After Adding Element at second position:-"+v);
System.out.println("Element at third position:-"+v.get(3));
System.out.println("First Element:-"+v.firstElement());
System.out.println("Last Element:-"+v.lastElement());
System.out.println("Is this vector empty?"+v.isEmpty());
}
}

/*Write a java program to implement thread life cycle.*/ 

import java.util.Vector;
class Pract7b
{
public static void main(String args[])
{
System.out.println(Thread.currentThread().getName());
for(int i=0;i<10;i++)
{
new Thread(""+i)
{
public void run()
{
System.out.println("Thread:"+getName()+"running");
}
}.start();
}
}
}

/*Write a java program to implement multithreading.*/

import java.io.*;
class A extends Thread
{
public void run()
{
System.out.println("Start A");
for(int i=1;i<=5;i++)
{
System.out.println("Thread A i:"+i);
}
System.out.println("Exit A");
}
}
class B extends Thread
{
public void run()
{
System.out.println("Start B");
for(int j=1;j<=5;j++)
{
System.out.println("Thread B j:"+j);
}
System.out.println("Exit B");
}
}
class C extends Thread
{
public void run()
{
System.out.println("Start C");
for(int k=1;k<=5;k++)
{
System.out.println("Thread C k:"+k);
}
System.out.println("Exit C");
}
}
class D extends Thread
{
public void run()
{
System.out.println("Start D");
for(int m=1;m<=5;m++)
{
System.out.println("Thread D m:"+m);
}
System.out.println("Exit D");
}
}
class Pract7c
{
public static void main(String args[])
{
new A().start();
new B().start();
new C().start();
new D().start();
}
}

/*Write a java program to open a file and display the contents in the console window.*/

import java.io.*;
public class Prac8a {
 public static void main(String[] args) throws FileNotFoundException, IOException {
 InputStream is=new FileInputStream("C:\\Users\\Ariba\\OneDrive\\Desktop\\java\\demo.txt");
 DataInputStream dis=new DataInputStream(is);
 int count= is.available();
 byte a[]=new byte[count];
 is.read(a);
 for (byte b : a) {
 char k=(char)b;
 System.out.print(k+"-");
 } }
}

/*Write a java program to copy the contents from one file to other files.*/

import java.io.*;
public class prac8b {
 public static void main(String[] args) throws FileNotFoundException, IOException {
 FileInputStream fis=null;
 FileOutputStream fos=null;
 try {
 File inF=new File("C:\\Users\\Ariba\\OneDrive\\Desktop\\java\\demo.txt");
 File outF=new File("C:\\Users\\Ariba\\OneDrive\\Desktop\\java\\Copied file.txt");
 fis=new FileInputStream(inF);
 fos=new FileOutputStream(outF);
 byte buff[]=new byte[1024];
 int length;
 while((length=fis.read(buff))>0)
 {
 fos.write(buff,0,length);
 }
 fis.close();
 fos.close();
 System.out.println("Contents Coppied...");
 } catch (Exception e) {
 e.printStackTrace();
} } }

/*Write a java program to read the student data from user and store it in the file.*/

import java.io.*;
import java.util.Scanner;
public class prac8c {
 public static void main(String[] args) throws FileNotFoundException, IOException {
 String s1,s2,s3;
 Scanner sc=new Scanner(System.in);
 System.out.println("Enter name: ");
 s1= sc.nextLine();
 System.out.println("Enter phone number");
 s2= sc.nextLine();
 System.out.println("Enter address: ");
 s3= sc.nextLine();
 OutputStream fos=new FileOutputStream("C:\\Users\\Ariba\\OneDrive\\Desktop\\java\\Student.txt");
 byte b1[]=s1.getBytes();
 fos.write(b1);
 byte b2[]=s2.getBytes();
 fos.write(b2);
 byte b3[]=s3.getBytes();
 fos.write(b3);
 fos.close();
 System.out.println("File Created");
 } 
}



