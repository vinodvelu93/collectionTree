# collectionTree
package javabasics;

import java.util.Iterator;
import java.util.TreeSet;

class Calc {


	public static void main(String[] args) {
		@SuppressWarnings("unchecked")
		TreeSet ref= new TreeSet (new Student1("date",78));
		Student1 s1= new Student1("xy",64);
		Student1 s2= new Student1("w",40);
		ref.add(s1);
		ref.add(s2);
		Iterator i= ref.iterator();
		while (i.hasNext()){
			System.out.println(i.next());
			
		}
		// TODO Auto-generated method stub

	}

}
class Student1 implements Comparator {

	
		int age;
		String name;
		 Student1() {
			// TODO Auto-generated constructor stub
		}
		Student1(String name, int age)
		{
			this.name=name;
			this.age=age;
		}
		
		public String toString()
		{
			return "Age==="+age;
		}
		
		@Override
		public int compare(Object o1, Object o2) {
			Student1 S1=(Student1)o1;
			Student1 S2=(Student1)o2;
			if(S1.age==S2.age)
			{
				return 0;}
				else if(S1.age>S2.age){
					return 1;
				}
				else{
					return -1;
			
			
		}

	

		}
}
