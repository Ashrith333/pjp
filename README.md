# pjp
codes
https://paste.ubuntu.com/p/mhxF8HzmvZ/
*#*#*#*#*#*
public class Main
{
	public static void main(String[] args) {
	int row =4,star = 2,inc =1;
	int hash,temp,sum=0;
	hash=star;for(int i=1;i<=row;i++)
	{
	    if(i!=1){
	        temp=(star*i)+(hash*(i-1));
	    }
	    else{
	        temp=star*i;
	    }
	    sum=temp+sum;
	    temp=0;
	    star=hash;
	    hash=star+inc;
	}
	System.out.println("sum: "+sum);
	}
}
Key address
public class Main
{
	public static void main(String[] args) {
	int address;
	int key;
	int sum=0;
	int counter=1;
	int arr[]={47,32,23,-15,12};
	int arrlen= arr.length;
	int i=0;
	while (counter<arrlen){
	    key=arr[i]%10;
	    address = arr[i]/10;
	    if(address<0){
	        key=key*-1;
	    }
	    if(counter%2 == 0){
	        sum=sum-key;
	    }
	    else{
	        sum=sum+key;
	    }
	    System.out.println(key+ " ");
	    if(arr[i]<0){
	        break;
	    }
	    counter++;
	    i=address;
	}
	if(counter == arrlen){
	    int max=-99;
	    for(int k=0;k<arrlen;k++){
	        if(arr[k] > max){
	            max=arr[k];
	        }
	    }
	    sum=max;
	}
	System.out.println();
	System.out.println(sum);
	}
}


Ororororoororor
import java.util.*;  
public class Main
{
	public static void main(String[] args) {
		int[] x ={47,32,74,49,65,-25,52,23};
		int k=0;
		int a=0,z;
		int sum=0;
		int i=0;
		List<Integer> ls= new ArrayList<Integer>();
		while(x[i]>0)
		{
		    while(x[i]>9){
		        k=x[i]%10;
		        x[i]=x[i]/10;
		        ls.add(k);
		        i=x[i];
		    }
		}
		k=(x[i]%10)*(-1);
		ls.add(k);
		for(int j=0;j<ls.size();j++)
		{
		    z=ls.get(j);
		    if(j%2 ==0)
		    {
		        sum = sum+z;
		    }
		    else{
		        sum=sum-z;
		    }
		}
		System.out.println(sum);
	}
}

Sum of three smallest digts from 5 digit number 
public class Main
{
    public int least(int n){
        String strn = Integer.toString(n);
        int length = strn.length();
        int n1=99,n2=99,n3=99;
        int flag1=0,flag2=0;
        for(int i=0;i<length;i++){
            int a =Integer.parseInt(String.valueOf(strn.charAt(i)));
            if(a<n1){
                n1=a;
                flag1=i;
            }
        }
        for(int j=0;j<length;j++){
             int b =Integer.parseInt(String.valueOf(strn.charAt(j)));
            if(b<n2 && j!=flag1){
                n2=b;
                flag2=j;
            }
        }
        for(int k=0;k<length;k++){
            int c =Integer.parseInt(String.valueOf(strn.charAt(k)));
            if(c<n3 && k!=flag1 && k!=flag2){
                n3=c;
            }
        }
        int sum=(n1*100) + (n2*10) + n3;
        return sum;
    }
	public static void main(String[] args) {
	    Main obj=new Main();
	    int sum=0;
	    int arr[]={32433,45414,12345,45789,84552};
	    for(int i = 0;i<arr.length;i++){
	        System.out.println(obj.least(arr[i]));
	        sum=sum+obj.least(arr[i]);
	    }
	    System.out.println("sum : " +sum);
	}
}
Sort string array based on int araay
public class Main
{
	public static void main(String[] args) {
		System.out.println("Hello World");
		int[] arr={10,2,5,4,3};
		String[] str={"Aravind","Bhanu","Ashrith","aakash","vamshi"};
		int temp;
		String temp1;
		for(int i=0;i<arr.length;i++)
		{
		    System.out.println(arr[i]+"--------->"+str[i]);
		    
		}
		
		for(int i=0;i<arr.length;i++)
		{
		    for(int j=i;j<arr.length;j++)
		    {
		        if(arr[i]>arr[j])
		        {
		            temp=arr[i];
		            arr[i]=arr[j];
		            arr[j]=temp;
		            
		            
		            temp1=str[i];
		            str[i]=str[j];
		            str[j]=temp1;
		            
		        }
		    }
		}
		
		System.out.println("After ssorting");
		for(int i=0;i<arr.length;i++)
		{
		    System.out.println(arr[i]+"--------->"+str[i]);
		    
		}
	}
}

GENERATE SERIES AND FING nth
       {
        int a=input1;
         int b=input2;
         int c=input3;
         int d=0;;
         int diff;
    for(int i=4;i<=input4;i++)
    {
        diff=b-a;
        d=c+diff;
        a=b;
        b=c;
        c=d;
    }
    return d;
    
        
    }
ENCODING 3 STRINGS(JOHN,JOHNY,JANARDAN)
{
String[] s={input1,input2,input3};
        String[] front=new String[3];
        String[] middle=new String[3];
        String[] end=new String[3];
    
        int l;
        for(int i=0;i<3;i++)
        {
            l=s[i].length();
            if(l%3==2)
            {
                front[i]=s[i].substring(0,(l/3)+1);
                middle[i]=s[i].substring((l/3)+1,2*(l/3)+1);
                end[i]=s[i].substring(2*(l/3)+1);
            }
            else if(l%3==1)
            {
                front[i]=s[i].substring(0,(l/3));
                middle[i]=s[i].substring((l/3),2*(l/3)+1);
                end[i]=s[i].substring(2*(l/3)+1);
            }
            else
            {
                front[i]=s[i].substring(0,(l/3));
                middle[i]=s[i].substring((l/3),2*(l/3));
                end[i]=s[i].substring(2*(l/3));
            }
        }
        String o1=front[0]+front[1]+front[2];
        String o2=middle[0]+middle[1]+middle[2];
        String o3=end[0]+end[1]+end[2];
        char[] c=o3.toCharArray();
        //String s3="";
        for(int j=0;j<c.length;j++)
        {
   
            if(c[j]>='A' && c[j]<='Z')
            {
               c[j]=Character.toLowerCase(c[j]);
               //s3=s3+c[j];
            }
            else
            {
                c[j]=Character.toUpperCase(c[j]);
                //s3=s3+c[j];
                System.out.println(c[j]);
            }
        }
      String o4=new String(c);
        Result res=new Result(o1,o2,o4);
        return res;
}
Print patients if in sequence
public static void main(String[] args) 
	    {
        int in1=10;
        String[] in2={"a","b","c","d","e","f","g","h","i","j"};
        int[] in3={2,6,12,7,9,15,10,11,16,12};
        int y=0,z=0,x=0,fl=0;
        for(int i=0;i<in1 && fl==0;i++)
        {
           x=i;
           for(int j=0;j<in1 && fl==0;j++)
           {
               if(in3[j]==in3[i]+1)
               {
                   y=j;
                   for(int k=0;k<in1;k++)
                   {
                       if(in3[k]==in3[j]+1)
                       {
                           z=k;
                           fl++;
                           //break;
                       }
                   }
               }
           }
        }
        System.out.println(in2[x]+":"+in2[y]+":"+in2[z]);
    }
}


GET CODE THROUGH STRINGS


String[] s=input1.split(" ");
		
		int l=0;
int sum=0;
int ans=0;
int r=0;
for(int i=0;i<s.length;i++)
{
	l=s[i].length();
	sum=sum+l;
}
while(sum>10)
{
	r=sum%10;
	sum=sum/10;
	ans=sum+r;
}
return ans;


SIMPLE ENCODED ARRAY
 
int[] a=new int[input2];
		int out1;
		int out2=0;
		a[input2-1]=input1[input2-1];
		for(int i=input2-1;i>0;i--)
		{
			a[i-1]=input1[i-1]-a[i];
			//System.out.println(i);
			//System.out.println(a[i]);
			out2=out2+a[i];
		
		}
		out2=out2+a[0];
		out1=a[0];
		
   Result r=new Result(out1,out2);
   return r;




DECREASING ORDER


		int max=1;
		int max2=0;
		int max1=0;
		for(int i=0;i<input2-1;i++)
		{
         if(input1[i]>input1[i+1])
		 {
			 max++;
		 }
		 else
		 {
			 if(max>1)
			 {
              max2++;                      //max=count the decreasing squence
					//max2=no of decreasing sequence
					//max1 =max length of sequnce

			   if(max1<=max)
			 {
				 max1=max;
			 }
			 }
			
			  max=1;
		 }
		 if(i==input2-2 && max>1)
		 {
			 max2++;
			 if(max1<=max)
			 {
				 max1=max;
			 }
		 }
		}
        Result r=new Result(max2,max1);
		return r;
    }
}




STABLE_UNSTABLE_PASSWORD


	int[] s={input1,input2,input3,input4,input5};
		
		int num=0;
		int stable_sum=0;
		int unstable_sum=0;
		int c=0;
		int d=0;
		int e=0;
		for(int i=0;i<s.length;i++)
		{ int[] count=new int[10];
			num=s[i];
			while(s[i]>0)
		{ 
			c=s[i]%10;
			count[c]++;
			s[i]=s[i]/10;
		}
		d=count[c];
for(int j=0;j<10;j++)
{
if(count[j]!=0)
{
	if(d==count[j])
	{
e=0;
}
else
{
e=1;
break;
}
}
}
if(e==0)
{
	stable_sum=stable_sum+num;
}
else
{
		unstable_sum=unstable_sum+num;

}

		}
		return stable_sum-unstable_sum;
	}



SUM OF NON PRIME INDEXES

int sum=0;
		int prime=0;
		int flag=0;
		for(int i=2;i<input2;i++)
		{flag=0;
			for(int j=1;j<=i/2;j++)
			{
				if(i%j==0&&j!=1)
				flag=1;
			}
			if(flag==0)
			{
			prime+=input1[i];
			System.out.println(prime);
			}
		}
		for(int i=0;i<input2;i++)
		{
			sum=sum+input1[i];
			//System.out.println(sum);
		}
		return sum-prime;
	}
\

PALINDROME REMOVE

	// Write code here...
		String reverse;
		int a = 0;
		String s=String.valueOf(input1);
		String b;
		StringBuffer x=new StringBuffer(s);
		String y=String.valueOf(x.reverse());
		if(s.equalsIgnoreCase(y))
		{
			a=-1;
		}
		else
		{
		for(int i=0;i<s.length();i++)
			{
				StringBuffer sb=new StringBuffer(s);
				sb.deleteCharAt(i);
				b = String.valueOf(sb);
				reverse=String.valueOf(sb.reverse());
				System.out.println(reverse + " " + s);
				if(reverse.equalsIgnoreCase(b))
				{
					a = i;
					break;
				}
			}
		}
			if(a == -1)
			{
				return a;
			}
			else
			{
				return Integer.parseInt(String.valueOf(s.charAt(a)));
		
	}
	
}



NAMBARIAR NUMBER

char[] c=input1.toCharArray();
		int[] x=new int[20];
		
	for(int i=0;i<c.length;i++)
	{
		x[i]=Character.getNumericValue(c[i]);
		//System.out.println(x[i]);
	}
	List<Integer> list=new ArrayList<Integer>();
	int sum=0;
	int count=0;
	for(int i=0;i<x.length;i++)
	{
		if(x[0]%2==0 && (sum%2==0 || sum==0))
		{
			sum=sum+x[i];
			count++;
		}
	else if(x[0]%2!=0 && (sum%2!=0 || sum==0))
	{
		sum=sum+x[i];
			count++;
	}
	else
	{
		x[0]=x[count];
		count++;
		list.add(sum);
		sum=x[0];
	}
	}
	list.add(sum);
String out="";
for(int i=0;i<list.size();i++)
{
	out=out+list.get(i);
}
int z=Integer.parseInt(out);
	return z;
	}




USER ID GENERATION
	String sn;
		String ln;
		String s2 =Integer.toString(input3);
	
		StringBuffer sb =new StringBuffer();
		if(input1.length()>input2.length())
		{
			sn=input2;
			ln=input1;
		}
		else if(input1.length()<input2.length())
		{
			sn=input1;
			ln=input2;
		}
		else
		{
			String[] s={input1,input2};
			Arrays.sort(s);
			sn=s[0];
			ln=s[1];
		}
		sb.append(sn.charAt(sn.length()-1));
		sb.append(ln);
		int n=input4;
		int l=s2.length();
		sb.append(s2.charAt(n-1));
		
		sb.append(s2.charAt(l-n));
		
		String xy= sb.toString();
		char[] c=xy.toCharArray();
		for(int i=0;i<c.length;i++)
{
	if(c[i]>='A' && c[i]<='Z')
	{
		c[i]=Character.toLowerCase(c[i]);
	}
	else
	{
		c[i]=Character.toUpperCase(c[i]);
	}
}
String x=new String(c);
System.out.println(x);
return x;


SUM OF dIGITS IN CYCLIC
{
int[] arr =new int[20];
		
		
		int b= Integer.toString(input1).length();
         int l=b;


		for(int i=0;i<b;i++)
		{
			arr[i]=input1%10;
			System.out.println(arr[i]);
		    input1=input1/10;
			
		}
		
		int sum=0;
		for(int i=0;i<b;i++)
		{
			sum=sum+l*arr[i];
			l--;
		}
}



MOST FREQUENT OCCURING:

	// Write code here...
		
{

              int count = 0;
		int maxResult = 0, outVal = 0;
		TreeMap<Integer, Integer> H1 = new TreeMap<>();
		for(int i = 0; i < input2; i++){
			String n = String.valueOf(input1[i]);
			for(int j = 0; j < n.length(); j++){
				int a = Integer.parseInt(String.valueOf(n.charAt(j)));
				System.out.println(a);
				if(H1.containsKey(a)){
					count = (Integer)H1.get(a);
					H1.put(a, count+1);
				}
				else{
					H1.put(a, 1);
				}
			}
		}
		System.out.println(H1);
		for(int k = 0; k <= 9; k++){
			if(H1.containsKey(k)){
				if(maxResult < H1.get(k)){
					maxResult = k;
				}
			}
		}
		System.out.println(maxResult);
		return maxResult;
	}





DECREASING SEQUENCE ..

{
   //Write code here...
       int ctr1=0;
	   int ctr2=0;
	   int d=1;
	   int max=0;
	   for(int i=0;i<input2-1;i++){
if(input1[i]>input1[i+1])
{ctr2++;
}
else if(input1[i+1]>input1[i]&&(ctr2!=0)){
	ctr1++;
	if(ctr2>max)
	max=ctr2+1;
	ctr2=0;
}
}
if((input2>2)&&input1[input2-1]<input1[input2-2])
{
	ctr1++;
	max++;
}
Result r=new Result(ctr1,max);
return r;



SUM OF NON PRIME INDEXES

int count=0;

int sum=0;

for(int i=0;i<input2;i++)

{

if(i==0 || i==1)

{

sum=input1[0]+input1[1];

}

else if(i==2)

{

}

else

{

for(int j=2;j<i;j++)

{

if((i%j)==0)

{

count=1;

}

}

if(count==1)

{

System.out.println(i+" "+sum);

count=0;

sum=sum+input1[i];

}

}

}

return sum;

}

String strNum = String.valueOf(input1);

StringBuffer finalStr = new StringBuffer();

String temp;

String revStr;

int pos = -1;

for(int i = 0; i < strNum.length(); i++){

// char charRem = strNum.charAt(i);

StringBuffer sb = new StringBuffer(strNum);

finalStr = sb.deleteCharAt(i);



WORLD WIDE WEB QUESTION:


Public int        

{
        int a;
        int b;
        int j=0;
        String s1=" ";
        int[] sum=new int[100];
        int[] num=new int[100]; 
        String[] s=input1.toUpperCase().split(" ");
        for(int i=0;i<s.length;i++)
        {
          a=0;
          sum[i]=0;
          b=s[i].length()-1;
          j=0;
           while(a!=b && a<b )
           {
               num[j]=Math.abs(s[i].charAt(a)-s[i].charAt(b));
               sum[i]=sum[i]+num[j];
                a++;
               b--;
               j++;
           }
           
           if(a==b)
           {
             num[j]=s[i].charAt(a)-64;
             sum[i]=sum[i]+num[j];
             
           }
           
          s1 =s1.concat(Integer.toString(sum[i]));
        }
        
      System.out.println(s1);
 
      String s2=s1.trim();
      int ans=Integer.parseInt(s2);
      return ans;
}

  IDENTIFY POSSIBLE WORDS


 {  int f=0;
        String ans1;
        String[] s=input2.toUpperCase().split(":");
        String ans=" ";
        int a=input1.indexOf('_');
        
        String[] replaced=input2.toUpperCase().split(":");
        for(int i=0;i<s.length;i++)
        {
        char[] c=s[i].toCharArray();
        c[a]='_';
        String b=new String(c);
        replaced[i]=b;  
        if(replaced[i].equals(input1.toUpperCase()))
        {
            f++;
            ans=ans+s[i]+":";   
        }
        }
        if(f>0)
        {
         ans1=ans.substring(1,ans.length()-1);   
        }
        else
        {
         ans1="ERROR-009";
        }
        return ans1;
}












ENCODING 3 STRINGS(JOHN,JOHNY,JANARDAN)
{
String[] s={input1,input2,input3};
        String[] front=new String[3];
        String[] middle=new String[3];
        String[] end=new String[3];
    
        int l;
        for(int i=0;i<3;i++)
        {
            l=s[i].length();
            if(l%3==2)
            {
                front[i]=s[i].substring(0,(l/3)+1);
                middle[i]=s[i].substring((l/3)+1,2*(l/3)+1);
                end[i]=s[i].substring(2*(l/3)+1);
            }
            else if(l%3==1)
            {
                front[i]=s[i].substring(0,(l/3));
                middle[i]=s[i].substring((l/3),2*(l/3)+1);
                end[i]=s[i].substring(2*(l/3)+1);
            }
            else
            {
                front[i]=s[i].substring(0,(l/3));
                middle[i]=s[i].substring((l/3),2*(l/3));
                end[i]=s[i].substring(2*(l/3));
            }
        }
        String o1=front[0]+front[1]+front[2];
        String o2=middle[0]+middle[1]+middle[2];
        String o3=end[0]+end[1]+end[2];
        char[] c=o3.toCharArray();
        //String s3="";
        for(int j=0;j<c.length;j++)
        {
   
            if(c[j]>='A' && c[j]<='Z')
            {
               c[j]=Character.toLowerCase(c[j]);
               //s3=s3+c[j];
            }
            else
            {
                c[j]=Character.toUpperCase(c[j]);
                //s3=s3+c[j];
                System.out.println(c[j]);
            }
        }
      String o4=new String(c);
        Result res=new Result(o1,o2,o4);
        return res;
}


  USERID GENERATION:

       {
         String ln;
        String sn;
        StringBuffer uid=new StringBuffer();
        //StringBuffer ln=new StringBuffer();
        if(input1.length()<input2.length())
        {
            sn=input1;
            ln=input2;
        }
        else if(input1.length()>input2.length())
        {
          sn=input2;
            ln=input1;  
        }
       else
       {
           String[] s4={input1,input2};
           Arrays.sort(s4);
          
           sn=s4[0];
           ln=s4[1];

       }
        uid.append(sn.charAt(sn.length()-1));
        uid.append(ln);
        uid.append(Integer.toString(input3).charAt(input4-1));
        int len=Integer.toString(input3).length();
        uid.append(Integer.toString(input3).charAt(len-input4));
        
        String s2=uid.toString();
        char[] c=s2.toCharArray();
        for(int j=0;j<c.length;j++)
        {
            
              
            if(c[j]>='A' && c[j]<='Z')
            {
               c[j]=Character.toLowerCase(c[j]);
               
            }
            else if(c[j]>='a' && c[j]<='z')
            {
                c[j]=Character.toUpperCase(c[j]);
                
                
            }
        }
      String ans=new String(c);

        return ans; 


GENERATE SERIES AND FING nth
       {
        int a=input1;
         int b=input2;
         int c=input3;
         int d=0;;
         int diff;
    for(int i=4;i<=input4;i++)
    {
        diff=b-a;
        d=c+diff;
        a=b;
        b=c;
        c=d;
    }
    return d;
    
        
    }




ALTERNATE ADD SUB
{
int a=input1;
        int sum=input1;
        int i;
        if(input2==1)
        {
         for(i=1;a>=1;i++)
          {
             if(i%2==1)
            
             {
                a--;
                sum=sum-a;
               
                System.out.println(sum+" "+a);
             }
             else
             {
                  a--;
                sum=sum+a;
               
                System.out.println(sum+" "+a);
             }
          }

        }
        else{
        for(i=1;a>=1;i++)
        {
            if(i%2==1)
            
            { 
                  a--;
                sum=sum+a;
             
                System.out.println(sum+" "+a);
            }
            else
            {
                 a--;
                sum=sum-a;
               
                System.out.println(sum+" "+a);
            }
        }

        }
        return sum;
    }	


NAMBIAR NUMBER
{
int z,num,sum=0,j=0;
        int[] sumarr=new int[20];
        boolean flag,check;
        for(int i=0;i<input1.length();i++)
        {
          num=(int)input1.charAt(i);
          z=i-1;
          if(num%2==0)
          {
              flag=true;
              check=false;
          }
          else
          {
              flag=false;
              check=true;
          }
          while(flag!=check && z<input1.length()-1)
          {
              z++;
             sum=sum+input1.charAt(z)-48;
            if(sum%2==0)
          {
              flag=true;
          }
          else
          {
              flag=false;
              
          }
            
          }
          sumarr[j]=sum;
          sum=0;
          j++;
          i=z;
          
        }
        String ans="";
        for(int k=0;k<j;k++)
        {

         ans=ans+""+sumarr[k];
        }
        
        return Integer.parseInt(ans);
        
    }


DECREASING SEQUENCE

{
int num=input1[0];
        int z=0,max=0;
        // int[] arr=new int[];
        int count=1;
        if(input2>1)
        {
        for(int i=1;i<input2;i++)
        {
            System.out.println("first"+i);
            if(input1[i]<num)
            {
             count++;
             if(i==input2-1)
             {
                 if(count>1)
                 {
                     z++;
                 }
                 if(max<count)
                 {
                    max=count;
                 }
             }
             num=input1[i];
             System.out.println(i);
            }
            else
            {

             if(count>1)
             {
                 if(max<count)
                 {
                    max=count;
                 }
               System.out.println(z+" "+count);
               z++;
              
             }
              count=1;
              num=input1[i];

            }
        }
        
        
        Result r=new Result(z,max);
        return r;
        }
        else
        {
            Result r=new Result(0,0);
         return r;
        }

    }



/////////////////////
int temp=0;
        int max=0;
        int ans=0;
        int count[]=new int[10];
        for(int i=0;i<input2;i++)
        {
            temp=input1[i];
            while(temp>0)
            {
               count[temp%10]++;
               temp=temp/10;
            }
        }
        for(int j=0;j<10;j++)
        {
        if(max<=count[j])
        {
            max=count[j];
            ans=j;
        }
        }
        return ans;
    }




