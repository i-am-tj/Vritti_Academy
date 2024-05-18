 ```java
 class toggle_case
 {
     toggle_case(char ch[])
     {
         for(int i=0;i<ch.length;i++)
         {
             if(ch[i]>='A' && ch[i]<='Z')
                 ch[i]=(char)(ch[i]+'a'-'A');
             else
                 if(ch[i]>='a' && ch[i]<='z')
                     ch[i]=(char)(ch[i]-'a'-'A');

         }

     }
 }
 public class Main
 {
    public static void main(String[] args)
    {
        String s= "ADityA";
        char[] stng=s.toCharArray();
        toggle_case str=new toggle_case(stng);
        System.out.println(stng);
    }
}

```