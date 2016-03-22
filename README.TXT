
Using the API


1. Download the API from http://www.sybero.in. Unzip the zipped file wherever you want.



2. Run hideDetails.jar



3. Add as much as entity you want:

    
	Ex:    	Entity Name: password

            
		Entity Value: 123@sybero



4. Now click ‘Encode Credentials’



5. You will see a new file has been created as ‘entities.sybo’. Copy this file and save it at safe place as it will act as the source of data.



6. Now import the hideDetails.jar in your project and copy ‘entities.sybo’ to your project folder. 
	The location will be as:

    
	In windows:

    
	C:\Users\Sybero Home\Documents\NetBeansProjects\<YourProjectName>



7. Sample program using this API:

    
	
	File name: Example.java


	
	
	import hidedetails.Entity;
 
	import hidedetails.EntityException;


	
	public class Example {

  		public static void main(String[] args) {
    
			try{
      
				Entity entity = new Entity();
      
				System.out.println(“user : ”+entity.getEntity(“username”));
      
				System.out.println(“pass : ”+entity.getEntity(“password”));
      
				System.out.println(“host : ”+entity.getEntity(“hostname”));
    
			}catch(EntityException e){
      
				System.out.println(e.getMessage());
    
			}    
  
		}
	
}

	
	Output:

	sybero

	123@sybero

	host.sybero



8. Now develop your project as you want, but remember to add ‘entities.sybo’ as your project source, the file must be in folder containing your built <YourProjectName>.jar during distribution.




How to edit or add some more details in ‘entities.sybo’ ?



For example you forget to add some password to the ‘entities.sybo’ file and you want to add these data right now. 
Simply delete previous ‘entities.sybo’ file and create a fresh file following the previouse process and add copy it to your project folder.



Have problem

If you have any issues/problem, feel free to contact me through rohit.sybero@rediffmail.com or rohit7209@rediffmail.com