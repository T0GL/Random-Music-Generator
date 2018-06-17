# Random-Music-Generator
It generates random music from direction that you choose.

As you can see it is so simple.
I wrote it and run with a .bat file.
I will give you the codes but you have to change them to use.
IT IS MY FIRST AND ONLY PROGRAM.

package deneme;

import java.io.File;
import java.io.IOException;
import java.util.Random;

public class RandomMusic {
	
	
	public static void main(String [] args){ 
		String path = "C:\\Users\\Fatih\\Desktop\\Beyin\\Music\\$aqoLera"; // change here
		File f = new File(path);
		File[] list = f.listFiles();
		Random r = new Random();
    // I have 117 files that's why there is a 117
		int random = r.nextInt(117);
		
        String[] strDosyalar = f.list();
        boolean nah = true;
        String muzik = null;
        while(nah) {
        	int w = 1;
        	
        for(String dosya : strDosyalar){
            /*System.out.println(w+ ". " + dosya);*/
            w++;           
            if(w == random){
             muzik =dosya;
            	nah=false;            	
            }
        }
        }
      	try {
					Runtime.getRuntime().exec("cmd /c start C:\\Users\\Fatih\\Desktop\\BEYIN\\Music\\$aqoLeRa\\" 
      	+ "\"" + muzik+ "\""); // obviously change here 
				} catch (IOException e) {
					// TODO Auto-generated catch block
					e.printStackTrace();
				}
		}	
	}
		



