/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package regexdfd;

/**
 *
 * @author luke
 */

import java.util.ArrayList;
import java.util.Scanner;
import javax.swing.JOptionPane;
public class Regexdfd {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
   String text;
        Scanner string = new Scanner(System.in);
        text = string.nextLine();
        System.out.println(text);
        String []split1;
            split1 = text.split("\\.");
            String part1=split1[0];
            //System.out.println(part1);
        String []split2;
        if(text.contains("I ")||text.contains("i ")){
            if(text.contains("I "))
                split2 = text.split("I have entities ");
            else
                split2 = text.split("i have entities ");
            String part2 = split2[1];
            //System.out.println(part2);
            String []split3 = part2.split(",");
            String part3 = split3[0];
            String part4 = split3[1];
            String part5 = split3[2];
            System.out.println(part3);
            System.out.println(part4);            
            String []splits5 = part5.split(". ");
            String spart4 = splits5[0];            
            System.out.println(spart4);
            
            //second sentence
            String secpart1=split1[1];
            String []secparts1 = secpart1.split("\\s\\.");
            String sec = secparts1[0];
            System.out.println(sec);
             
            //third sentence
            String tdpart1=split1[2];
            String []tdparts1 = tdpart1.split("\\s\\.");
            String trd = tdparts1[0];
            System.out.println(trd);            
            
    }
        else
            System.out.println("Invalid");
        
    }
}

    
