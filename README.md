# zigzag-array-haccerank-
Wipro Talent Next 2017-2021 Batch
Stream
Classwork
People
Wipro Talent Next 2017-2021 Batch
Meet link
https://meet.google.com/lookup/hm6wjlx6dr

Share something with your class…

Announcement: "75 students have not attended Mock…"
Ashok M
Created 1:30 PM1:30 PM
75 students have not attended Mock Test-9


Announcement: "Toppers in Java Mock Test-9 -…"
Ashok M
Created 1:11 PM1:11 PM
Toppers in Java Mock Test-9 - 13.06.2020

Aswini S
Durgadevi S
Kiruthika V
Mukesh Kanna S
Nasima Banu A
Nikitha Keerthana S R
Revathi S
S R Keerthi
Sujithra R
Vigneshwar K

Assignment: "Wipro Java Mock Test-9"
Ashok M posted a new assignment via Quizizz: Wipro Java Mock Test-9
Created 11:51 AM11:51 AM

Announcement: "Top Coders - Hackerrank TalentNext…"
Maria Michael Visuwasam L
Created 11:02 AM11:02 AM
Top Coders - Hackerrank TalentNext Test-13 - Congratulations
Jaya sree
Janani K
JAYASHREE R
Kowsalyaa V
Nikitha  Keerthana
nishiha 
Priyanka Srinivasan
Saravanan Jayakumar
Keerthi. S. R.
vigneshwar.k.2017.cse@ritchennai.edu.in   
 


Announcement: "Hackerrank TalentNext Test-12 - Top…"
Maria Michael Visuwasam L
Created Jun 12Jun 12
Hackerrank TalentNext Test-12 - Top Coders - Congratulations

M.Jawahar 
Jaya sree
Amirthavarshini  R B
Nikitha  Keerthana
Koushik Ram
JAYASHREE R
vigneshwar.k.2017.cse@ritchennai.edu.in   
Ganesh S
Kowsalyaa V
Saravanan Jayakumar
Keerthi. S. R.


Announcement: "131 students have not attended Mock…"
Ashok M
Created Jun 11Jun 11
131 students have not attended Mock Test-8


Announcement: "Toppers in Java Mock Test-8 -…"
Ashok M
Created Jun 11Jun 11
Toppers in Java Mock Test-8 - 11.06.2020

Nasima A
Vigneshwar K 
Aswini S 

Assignment: "Wipro Java Mock Test-8"
Ashok M posted a new assignment via Quizizz: Wipro Java Mock Test-8
Created Jun 11Jun 11 (Edited Jun 11)

Announcement: "Top Coders - Hackerrank TalentNext…"
Maria Michael Visuwasam L
Created Jun 11Jun 11
Top Coders - Hackerrank TalentNext Test-11 - Congratulations

Arunaa Ganthimathi
S. Aswini
Dhivya S
Divya Bharathy Venkatraman
DURGADEVI S
geethika annem
Janani K
JAYASHREE R
kallish kumar.N
Kowsalyaa V
Nikitha  Keerthana
sagayasree.z.2017.cse@ritchennai.edu.in 
Keerthi. S. R.
vigneshwar.k.2017.cse@ritchennai.edu.in   
VIGNESH WARAN


Announcement: "94 students have not attended Mock…"
Ashok M
Created Jun 10Jun 10
94 students have not attended Mock Test-7


Announcement: "Toppers in Java Mock Test-7 -…"
Ashok M
Created Jun 10Jun 10
Toppers in Java Mock Test-7 - 10.06.2020
Aswini S
Vigneshwar K


Assignment: "Wipro Java Mock Test-7"
Ashok M posted a new assignment via Quizizz: Wipro Java Mock Test-7
Created Jun 10Jun 10

Announcement: "Hackerrank Problem - Product Sort -…"
Maria Michael Visuwasam L
Created Jun 10Jun 10
Hackerrank Problem - Product Sort - Solution

class Result {

    /*
     * Complete the 'itemsSort' function below.
     *
     * The function is expected to return an INTEGER_ARRAY.
     * The function accepts INTEGER_ARRAY items as parameter.
     */
    public static List<Integer> itemsSort(List<Integer> items) {
    // Write your code here
        int size=items.size();
        int[][] arr=new int[size][2];
        int i=0,index=0;
        while(i<size){
            int temp=0,x=0;
            for(int j=0;j<index;j++){
                if(arr[j][0]==items.get(i)){
                    temp=1;
                    x=j;
                }
            }
            if(temp==0){
                arr[index][0]=items.get(i);
                arr[index][1]=1;
                index++;
            }
            else{
                arr[x][1]++;
            }
            i++;
        }
        for(i=0;i<index-1;i++){
            for(int j=i+1;j<index;j++){
                if(arr[i][1]>arr[j][1]){
                    int temp1=arr[i][0];
                    int temp2=arr[i][1];
                    arr[i][0]=arr[j][0];
                    arr[i][1]=arr[j][1];
                    arr[j][0]=temp1;
                    arr[j][1]=temp2;
                }
                if(arr[i][1]==arr[j][1]){
                    if(arr[i][0]>arr[j][0]){
                    int temp1=arr[i][0];
                    int temp2=arr[i][1];
                    arr[i][0]=arr[j][0];
                    arr[i][1]=arr[j][1];
                    arr[j][0]=temp1;
                    arr[j][1]=temp2;
                    }
                }
            }
        }
        List<Integer> list=new ArrayList<Integer>();
        for(i=0;i<index;i++){
            for(int j=0;j<arr[i][1];j++){
                list.add(arr[i][0]);
            }
        }
        return list;
    }
}


Announcement: "Hackerrank Problem - Bob Navigates a…"
Maria Michael Visuwasam L
Created Jun 10Jun 10
Hackerrank Problem - Bob Navigates a Maze

class Result {

    /*
     * Complete the 'minMoves' function below.
     *
     * The function is expected to return an INTEGER.
     * The function accepts following parameters:
     *  1. 2D_INTEGER_ARRAY maze
     *  2. INTEGER x
     *  3. INTEGER y
     */

    static int[][][] dist;
    static int[][] dp;
    static List<int[]> coins;
    static int R;
    static int C;
    static int allOnes, numCoins;
    static int MAXDIST = 1000 * 1000;
    static boolean isInRange(int r, int c) {
        return r >= 0 && r < R && c >= 0 && c < C;
    }
    static void extractCoins(List<List<Integer>> arr, List<int[]> coins) {
        for (int r = 0; r < R; r++) {
            for (int c = 0; c < C; c++) {
                if (arr.get(r).get(c) == 2) {
                    int[] point = {r, c};
                    coins.add(point);
                }
            }
        }
    }
    static void setDistances(List<List<Integer>> arr, int coin) {
        for (int r = 0; r < R; r++) {
            for (int c = 0; c < C; c++) dist[r][c][coin] = MAXDIST;
        }
        boolean[][] visited = new boolean[R][C];
        Queue<int[]> q = new LinkedList<>();
        int[] startPoint = coins.get(coin);
        q.add(startPoint);
        visited[startPoint[0]][startPoint[1]] = true;
        dist[startPoint[0]][startPoint[1]][coin] = 0;
        int[] dr = {0, -1, 0, 1};
        int[] dc = {-1, 0, 1, 0};
        while (!q.isEmpty()) {
            int[] point = q.poll();
            int oldR = point[0];
            int oldC = point[1];
            for (int k = 0; k < 4; k++) {
                int newR = oldR + dr[k];
                int newC = oldC + dc[k];
                if (isInRange(newR, newC) && !visited[newR][newC] && arr.get(newR).get(newC) != 1) {
                    int[] newPoint = {newR, newC};
                    visited[newR][newC] = true;
                    dist[newR][newC][coin] = dist[oldR][oldC][coin] + 1;
                    q.add(newPoint);
                }
            }
        }
    }
    public static int minMoves(List<List<Integer>> maze, int x, int y) {
    // Write your code here
        R = maze.size();
        C = maze.get(0).size();
        int[] startPoint = {0, 0};
        coins = new ArrayList<>();
        coins.add(startPoint);
        extractCoins(maze, coins);
        numCoins = coins.size();
        allOnes = (1 << numCoins) - 1;
        int dpR = numCoins;
        int dpC = allOnes + 1;
        dp = new int[dpR][dpC];
        for (int i = 0; i < dpR; i++) {
            for (int j = 0; j < dpC; j++) dp[i][j] = -1;
        }
        dist = new int[R][C][numCoins];
        for (int i = 0; i < numCoins; i++) setDistances(maze, i);
        int ans = getMinDist(0, 1, x, y);
        return ans >= MAXDIST ? -1 : ans;
    }
    static int getMinDist(int coin, int seq, int Ra, int Ca) {
        if (seq == allOnes) return dist[Ra][Ca][coin];
        if (dp[coin][seq] != -1) return dp[coin][seq];
        int res = Integer.MAX_VALUE;
        for (int i = 0; i < numCoins; i++) {
            if ((seq & (1 << i)) == 0) {
                int newSeq = seq | (1 << i);
                int[] pos = coins.get(i);
                res = Math.min(res, getMinDist(i, newSeq, Ra, Ca) + dist[pos[0]][pos[1]][coin]);
            }
        }
        dp[coin][seq] = res;
        return res;
    }
}


Announcement: "Hackerrnk Problem - Price Check -…"
Maria Michael Visuwasam L
Created Jun 10Jun 10
Hackerrnk Problem - Price Check - Solution

class Result {

    /*
     * Complete the 'priceCheck' function below.
     *
     * The function is expected to return an INTEGER.
     * The function accepts following parameters:
     *  1. STRING_ARRAY products
     *  2. FLOAT_ARRAY productPrices
     *  3. STRING_ARRAY productSold
     *  4. FLOAT_ARRAY soldPrice
     */

    public static int priceCheck(List<String> products, List<Float> productPrices, List<String> productSold, List<Float> soldPrice) {
    // Write your code here
    int error = 0, i, j;
    for(i=0; i<productSold.size(); i++)
    {
        String str = productSold.get(i);
        for(j=0; j<products.size(); j++)
        {
            String st = products.get(j);
            if(st.equals(str))
                break;
        }
        if(!(soldPrice.get(i).equals(productPrices.get(j))))
            error++;
    }
    return error;
    }
}


Announcement: "Top Coders - Talent Next Test-10 -…"
Maria Michael Visuwasam L
Created Jun 9Jun 9
Top Coders - Talent Next Test-10 - Congratulations

Nikitha  Keerthana
S. Aswini
Saravanan Jayakumar
Ranjith veda


Announcement: "Toppers in Java Mock Test-6 -…"
Ashok M
Created Jun 9Jun 9
Toppers in Java Mock Test-6 - 09.06.2020
Janani K
Kallish Kumar N
Kishore S
Vigneshwar K


Announcement: "CSS&CSS 3 REFERENCE TUTORIALS"
Maria Michael Visuwasam L
Created Jun 9Jun 9
CSS&CSS 3 REFERENCE TUTORIALS

CSS 3 TUTORIAL.doc

CSS Tutorial_examples.doc

Assignment: "Wipro Java Mock Test-6"
Ashok M posted a new assignment via Quizizz: Wipro Java Mock Test-6
Created Jun 9Jun 9

Announcement: "Toppers in Java Mock Test-5 -…"
Ashok M
Created Jun 8Jun 8
Toppers in Java Mock Test-5 - 08.06.2020

Harini V R
Janani K
Jayasree M
Kishore S
Nagella Kishore Kumar Reddy
Praveena R
Sandhiya K
Suryaprakash A
Thamarai Selvan U
Vigneshwar K


Announcement: "Top Coders - TalentNext Test-9 -…"
Maria Michael Visuwasam L
Created Jun 8Jun 8
Top Coders - TalentNext Test-9 - Congratulations

Jaya sree
Nikitha  Keerthana
Saravanan Jayakumar
Ganesh S
R.Raghual ravi
subhathra E k


Announcement: "HTML Reference"
Maria Michael Visuwasam L
Created Jun 8Jun 8
HTML Reference

HTML.doc


Announcement: "HTML Reference"
Maria Michael Visuwasam L
Created Jun 8Jun 8
HTML Reference

HTML.doc

Assignment: "Wipro Java Mock Test-5"
Ashok M posted a new assignment via Quizizz: Wipro Java Mock Test-5
Created Jun 8Jun 8

Announcement: "Top Coders - Hackerrank TalentNext Test…"
Maria Michael Visuwasam L
Created Jun 6Jun 6
Top Coders - Hackerrank TalentNext Test - Congratulations

S. Aswini
Divya Bharathy Venkatraman
DURGADEVI S
V.R.Harini 
Janani K
jayashree ravi kumar
geethika annem
Nikitha  Keerthana
Saravanan Jayakumar
Aarthi lakshmipathi
Ameen Ur Rahman K
Aravind padmanaban
Arunaa Ganthimathi
bathri narayanan
Danielraja Jeyachandran
Dhivya S
hari narayanan s
Hemanth T
Padmavathy R


Announcement: "Session PPTs"
Ashok M
Created Jun 6Jun 6
Session PPTs

Wipro_JavaTraining_Day23.pptx

Wipro_JavaTraining_Day24.pptx


Announcement: "Toppers in Mock Test-4 - 06.06.2020…"
Ashok. Java
Created Jun 6Jun 6
Toppers in Mock Test-4 - 06.06.2020

Arul Selsiya L
Aswini S
Kishore S
Ramya S
Sandhiya K
Snehitha G


Announcement: "63 students have not attended the Mock…"
Ashok. Java
Created Jun 6Jun 6
63 students have not attended the Mock Test-4

Assignment: "Wipro Java Mock Test-4"
Ashok M posted a new assignment via Quizizz: Wipro Java Mock Test-4
Created Jun 6Jun 6

Announcement: "Take this self Assessment in Java…"
Ashok M
Created Jun 5Jun 5
Take this self Assessment in Java

https://www.w3schools.com/java/java_exercises.asp


Announcement: "Top Coders - TalentNext Test-7 -…"
Maria Michael Visuwasam L
Created Jun 5Jun 5
Top Coders - TalentNext Test-7 - Congratulations

Nikitha  Keerthana
saikailash.s.2017.cse@ritchennai.edu.in 
Saravanan Jayakumar
sowmiya.s.2017.cse@ritchennai.edu.in 
vigneshwar.k.2017.cse@ritchennai.edu.in   
shanthosh kp
Suresh A S


Announcement: "Session PPTs"
Ashok. Java
Created Jun 5Jun 5
Session PPTs

Wipro_JavaTraining_Day22.pptx

Wipro_JavaTraining_Day21.pptx


Announcement: "62 students have not attended Mock…"
Ashok. Java
Created Jun 5Jun 5
62 students have not attended Mock Test-3


Announcement: "Toppers in Mock Test-3 - 05.06.2020…"
Ashok. Java
Created Jun 5Jun 5
Toppers in Mock Test-3 - 05.06.2020

Harini V R
Nasima Banu A
Nivetha R
Sandhiya K

Assignment: "Core Java Mock Test-3"
Ashok M posted a new assignment via Quizizz: Core Java Mock Test-3
Created Jun 5Jun 5

Announcement: "Bit Logic - Hackerrank Solution class…"
Maria Michael Visuwasam L
Created Jun 4Jun 4
Bit Logic - Hackerrank Solution

class Result {

    /*
     * Complete the 'maxXor' function below.
     *
     * The function is expected to return an INTEGER.
     * The function accepts following parameters:
     *  1. INTEGER lo
     *  2. INTEGER hi
     *  3. INTEGER k
     */

    public static int maxXor(int lo, int hi, int k) {
    int i,j;
    int big=0;
    int temp;
    for (i=lo;i<hi;i++)
    {
        for (j=lo+1;j<=hi;j++)
        {
            temp = i^j;
            if (temp<=k&&big<temp)
            {
                big=temp;
            }
        }
    }
    return big;

    }

}


Announcement: "Account Comparison - Hackerrank…"
Maria Michael Visuwasam L
Created Jun 4Jun 4
Account Comparison - Hackerrank Solution

class Account implements OnlineAccount, Comparable<Account> {

    int noOfRegularMovies, noOfExclusiveMovies;
    String ownerName;

    // 1) Add a parameterized constructor that initializes the attributes noOfRegularMovies and noOfExclusiveMovies.
    Account (String oname,int nrm, int nem)
    {
        this.ownerName = oname;
        this.noOfRegularMovies=nrm;
        this.noOfExclusiveMovies=nem;
    }

    // 2. This method returns the monthly cost for the account.
    public int monthlyCost() {
            return basePrice + (noOfRegularMovies*regularMoviePrice) + (noOfExclusiveMovies*exclusiveMoviePrice);
    }

    // 3. Override the compareTo method of the Comparable interface such that two accounts can be compared based on their monthly cost.
    @Override
    public int compareTo(Account o) {
        // TODO Auto-generated method stub
        if (this.monthlyCost()>o.monthlyCost())
        {
            this.toString();
            return 1;
        }
        else
        {
            o.toString ();
            return -1;
        }
        
    }
    
    // 4. Returns "Owner is [ownerName] and monthly cost is [monthlyCost] USD."
    public String toString() {
        String s = new String ();
        s="Owner is " + ownerName + " and monthly cost is " + monthlyCost() + " USD.";
        return s;

    }
}


Announcement: "Car Inheritance - Hackerrank Solution…"
Maria Michael Visuwasam L
Created Jun 4Jun 4
Car Inheritance - Hackerrank Solution

class WagonR extends Car
{
    int mil;
    public WagonR (int n)
    {
        super(false, "4");
        this.mil=n;
           
    }
    public String getMileage ()
    {
        String s = new String ();
        s= mil + " kmpl";
        return s;
    }

}


/**
*   HondaCity class
**/
class HondaCity extends Car
{
    int mil;
    public HondaCity (int n)
    {
        super(true, "4");
        mil=n;
    }
    public String getMileage ()
    {
        String s = new String ();
        s= mil + " kmpl";
        return s;
    }
}
/**
*   InnovaCrysta class
**/
class InnovaCrysta extends Car
{
    int mil;
    public InnovaCrysta (int n)
    {
        super(false,"6");
        mil=n;
    }
    public String getMileage ()
    {
        String s = new String ();
        s= mil + " kmpl";
        return s;
    }
    
}


Announcement: "Hackerrank TalentNext Test-6 - TOP…"
Maria Michael Visuwasam L
Created Jun 4Jun 4
Hackerrank TalentNext Test-6 - TOP CODERS LIST - Congratulations

Hemanth T
Saravanan Jayakumar
sowmiya.s.2017.cse@ritchennai.edu.in 
vigneshwar.k.2017.cse@ritchennai.edu.in   
Keerthi. S. R.
VIGNESH WARAN
R.jagannathan 
C.Jayakumar 
Jeswanth kumar
Kr Keerthana
krudhash N
MOHAN RAJ.S
Nivetha R
Aarthi lakshmipathi
Ameen Ur Rahman K
Amirthavarshini  R B
Aravind padmanaban
S. Aswini
geethika annem
V.R.Harini 
Jaichandran S
Janani K
Jaya sree
jayashree ravi kumar
Mannoj 
mohamed ibrahim
Nikitha  Keerthana
priyadharshini.s 



Announcement: "Hackerrank Test - Count String…"
Maria Michael Visuwasam L
Created Jun 4Jun 4
Hackerrank Test - Count String Permutations - Solution

class Result {

    /*
     * Complete the 'countPalindromes' function below.
     *
     * The function is expected to return an INTEGER.
     * The function accepts STRING s as parameter.
     */

    public static int countPalindromes(String s) {
    // Write your code here
int count = 0;
        if (s == null || s.length() == 0) {
            return count;
        }
        boolean[][] dp = new boolean[s.length()][s.length()];
        for (int i = 0; i < s.length(); i++) {
            dp[i][i] = true;
            count++;
        }
        for (int i = 1; i < s.length(); i++) {
            if (s.charAt(i - 1) == s.charAt(i)) {
                dp[i - 1][i] = true;
                count++;
            }
        }
        for (int j = 2; j < s.length(); j++) {
            for (int i = 0; i < j; i++) {
                if (dp[i + 1][j - 1] && s.charAt(i) == s.charAt(j)) {
                    dp[i][j] = true;
                    count++;
                }
            }
        }
        return count;
    }
    

    }



Announcement: "Hackerrank Test - Palindrome Counter -…"
Maria Michael Visuwasam L
Created Jun 4Jun 4
Hackerrank Test - Palindrome Counter - Solution

class Result {

    /*
     * Complete the 'countPalindromes' function below.
     *
     * The function is expected to return an INTEGER.
     * The function accepts STRING s as parameter.
     */

    public static int countPalindromes(String s) {
    // Write your code here
int count = 0;
        if (s == null || s.length() == 0) {
            return count;
        }
        boolean[][] dp = new boolean[s.length()][s.length()];
        for (int i = 0; i < s.length(); i++) {
            dp[i][i] = true;
            count++;
        }
        for (int i = 1; i < s.length(); i++) {
            if (s.charAt(i - 1) == s.charAt(i)) {
                dp[i - 1][i] = true;
                count++;
            }
        }
        for (int j = 2; j < s.length(); j++) {
            for (int i = 0; i < j; i++) {
                if (dp[i + 1][j - 1] && s.charAt(i) == s.charAt(j)) {
                    dp[i][j] = true;
                    count++;
                }
            }
        }
        return count;
    }
    }


Announcement: "Hackerrank Test - Programming Contest -…"
Maria Michael Visuwasam L
Created Jun 4Jun 4
Hackerrank Test -  Programming Contest - Solution

class Result {

    /*
     * Complete the 'minimizeBias' function below.
     *
     * The function is expected to return an INTEGER.
     * The function accepts INTEGER_ARRAY ratings as parameter.
     */

    public static int minimizeBias(List<Integer> ratings) {
    // Write your code here
        int sum=0;
        int len = ratings.size();
        Collections.sort(ratings);
        for(int i=0; i<len-1; i+=2){
            int diff = ratings.get(i+1)-ratings.get(i);
            sum+= diff;
        }
        return sum;
    }
}


Announcement: "Hackerrank Test - ZIG ZAG ARRAY -…"
Maria Michael Visuwasam L
Created Jun 4Jun 4
Hackerrank Test - ZIG ZAG ARRAY - SOLUTION

import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.function.*;
import java.util.regex.*;
import java.util.stream.*;
import static java.util.stream.Collectors.joining;
import static java.util.stream.Collectors.toList;
import java.util.Scanner;

public class Zigzag {
    public static void main(String[] args) {
        int a[],b,count=0,counts=0;
        Scanner in=new Scanner(System.in);
        b=in.nextInt();
        a=new int[b];
        int sub=0,sum=0;
        for(int i=0;i<b;i++)
        {    int c=in.nextInt();
            a[i]=c;
        }
        for(int j=0;j<b-2;j++)
        {
            if(j%2==0)
            {
                if(a[j]<a[j+1])
                {
                    continue;
                }
                else
                {
                    a[j+1]=0;
                    j++;
                    count++;
                }
            }
            else
            {
                if(a[j]>a[j+1])
                {
                    continue;
                }
                else
                {
                    a[j+1]=0;
                    j++;
                    count++;
                }
            }
        }
        
        for(int k=0;k<b-2;k++)
        {
            if(k%2==0)
            {
                if(a[k]>a[k+1])
                {
                    continue;
                }
                else
                {
                    a[k+1]=0;
                    k++;
                    counts++;
                }
            }
            else
            {
                if(a[k]<a[k+1])
                {
                    continue;
                }
                else
                {
                    a[k+1]=0;
                    k++;
                    counts++;
                }
            }
        }
        if(count<counts)
        {
            System.out.println(count);
        }
        else
        {
            System.out.println(counts);
        } 
    }
}
