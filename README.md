# span-of-an-element-in-array
/*package whatever //do not write package name here */

import java.io.*;
import java.util.*;

class GFG {
	public void span(int arr[],int n) 
	{
	    Stack<Integer>s=new Stack<Integer>();
	    for(int i=0;i<n;i++)
	    {
	        while(s.empty()==false && arr[s.peek()]<=arr[i])
	        {
	            s.pop();
	        }
	        int spa=(s.empty())?i+1:(i-s.peek());
	        System.out.println(arr[i]+" "+spa);
	        s.push(i);
	    }
	    
	}
	public static void main (String[] args) {
	    GFG sl=new GFG();
	    
	    int arr[]={15,13,12,14,16,8,6,4,10,30};
	    int n=arr.length;
	    sl.span(arr,n);
	}
}
