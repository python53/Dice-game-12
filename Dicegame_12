/*Tärningsspel 12, Uppgift_3 Java
 *
 * Variabler skapas
 *    Tärningarna ligger inom yttre loppen för att kunna, för att kunna avgöra vinst eller förlust.
 * 
 * Inre loop, tärningarna slås, System.out.format(.....) används för att få in multipla argument. arg.toString(): %s - https://docs.oracle.com/javase/tutorial/java/data/numberformat.html
 *    else finns med under varje case ifall man råkar slå samma tärning två gånger. 
 * 
 * Vinster och förluster skrivs ut i efterhand. Detta då det i uppgiften var oklart om det skulle skrivas ut i denna omgång eller nästa.
 * på bifogad bild ser man att förluster inte presenteras i nuvarande omgång men vinster gör. Så mitt val blev att presentera vinst och förlust i kommande omgång. 
 * 
 * *Increment operator; increments a value by 1. Dvs ökar värdet med 1, då villkoret: summa_vid_vinst == summan_av_tarningar är uppfyllt. https://docs.oracle.com/javase/tutorial/java/nutsandbolts/opsummary.html
 *
 * @author Nicklas Svensson, nicsve-1
 * 
 * */



import java.util.Scanner;

public class Uppgift3_case
{
   
   public static void main(String[] args)
   {
      /* Variabler
       * Konstanta värden; antal sidor på tärningen
       * Scanner för userinput 
       * Samt välkomstmeddelande
       */
      int summa_vid_vinst = 12, vinster = 0, forluster = 0, antal_sidor_tarning = 6, summan_av_tarningar = 0;     
      
      
      Scanner fetch = new Scanner(System.in);
      
      System.out.format("Välkommen till spelet 12. Du ska slå 1-3 tärningar och försöka få summan 12... \n");
      
      do 
      {
         int tarning_1 = 0, tarning_2 = 0, tarning_3 = 0;
         
         do 
         {
         System.out.format("Ange vilken tärning du vill slå [1,2,3](avsluta med q): ");
         
            switch (fetch.nextLine())
            {
            case "1": //slå tärning 1
               if (tarning_1 == 0) 
               {
                  tarning_1 = 1+(int)(Math.random()*antal_sidor_tarning);
                  break;
               }
               
               else 
               {
                  System.out.format("Tärning redan slagen, vänligen välj tärning 2 eller 3. Om du önskar avbryta, vänligen tryck q \n");
                  break;
               }
                
            case "2": //slå tärning 2
               if (tarning_2 == 0) 
               {
                  tarning_2 = 1+(int)(Math.random()*antal_sidor_tarning);
                  break;
               }
               
               else 
               {
                  System.out.format("Tärning redan slagen, vänligen välj tärning 1 eller 3. Om du önskar avbryta, vänligen tryck \n");
                  break;
               }
               
            case "3": //slå tärning 3
               if (tarning_3 == 0) 
               {
                  tarning_3 = 1+(int)(Math.random()*antal_sidor_tarning);
                  break;
               }
               
               else 
               {
                  System.out.format("Tärning redan slagen, vänligen välj tärning 1 eller 2. Om du önskar avbryta, vänligen tryck q");
                  break;
               }
               
            case "q": //avbryta spelet
               System.out.format("Avslutar spel!");
               System.exit(0);
               break;
               
            default:
               System.out.println("Felaktigt värde, vänligen försök igen");
               break;
            }
            summan_av_tarningar = (tarning_1 + tarning_2 + tarning_3);
            System.out.format("%s %s %s sum: %s #vinst: %s #förlust: %s \n", tarning_1, tarning_2, tarning_3, summan_av_tarningar, vinster, forluster);
            
                        
         //Booleans för att sätta gränser, för när spelat är över
         }while((tarning_1 == 0 || tarning_2 == 0 || tarning_3 == 0) && summan_av_tarningar != summa_vid_vinst);     
         
         if (summa_vid_vinst == summan_av_tarningar)
         {
            vinster++; //*
         }
         
         else 
         {
            forluster++; //*
         } 
            
            
         System.out.format("Nästa omgång! \n");
         
      }while(true);
      
      
   }
   
}
