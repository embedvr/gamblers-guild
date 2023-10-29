<script>
    import { Button, buttonVariants } from "$lib/components/ui/button";
    import * as Dialog from "$lib/components/ui/dialog";
    import { Input } from "$lib/components/ui/input";
    import { Label } from "$lib/components/ui/label";
</script>

<div class="flex flex-col md:gap-4 gap-16 items-center text-center px-8 py-8">
    <pre
        tabindex="-1"
        id="output"
        style="white-space: pre;
  font-family: monospace;
  font-size: 6px;
  line-height: 6px;
  letter-spacing: unset;
  transform: unset;
  overflow-y: hidden;">                                                                                        
                                                                                        
                                      ##+-         -#                                   
                          ##-                          -#                               
                  #-                       #########+      #                            
             #                              .#########        #                         
           #            ########                                 #                      
          #..           ##########                                  #                   
          ......          .######.                                     #                
          .........                                                       #             
         #...........                                       ########        +           
         .. ...........                                     +#########.                 
         .. .............                                      +######           #      
        # ....####..........            #########-                                #     
        # .. ######...........           ##########                           ....      
        -.. .#######............            .+###.                      .......  ..     
         .  .-######..............                                .......... ..   #     
          . ..#####-................                         ...............  .. .      
       # .. ....+#...................                  ..................  ..    #      
       # .   . ........................  .        ..................+##### ..           
       +  . .  .. ...................... .     ....................########  .. +       
       - ..... .. .......................    ....................-########-             
       .     . .....###...................  .....................######### .   #        
         .  .   .  #####-................  ......................########     .         
          .. .... -######................ ..................... ..#####  .              
              .  ..#######............... .................... ...           -          
         . .    ...-#####-............... ..................  .   . .                   
          . . ..  .. ###+............... ................... ...  .         +           
       .     . .  .. ................... ................  ..  .                        
            .   . . .....................................  ..  .                        
         +   .   .   .. ..............................  ..                +             
             ..  .. .. . ........................... .. ..  ..                          
            #     .  .. -####.................... ###-.                  #              
              ..  .  . .######+.................#######  .              -               
                  .. . .#######...............######### .                               
                 #  .  ..######...............########+                                 
                   + . . .#####..............#########                                  
                     . . ..................  -######             .#                     
                       .  . ............. .. ...-.            #                         
                         . . ...........  ..             .#                             
                          #.. ........ .. .         .+                                  
                            # . .....  ..  ...  +                                       
                               . .. .. .  .#                                            
                                 #-.-#                                                  
                                                                                        
                                                                                        
</pre>
    <div class="flex flex-col md:flex-row">
        <pre class="harry" tabindex="-1">
ooooooooooooo oooo                    
8'   888   `8 `888                    
     888       888 .oo.    .ooooo.    
     888       888P"Y88b  d88' `88b   
     888       888   888  888ooo888   
     888       888   888  888    .o   
    o888o     o888o o888o `Y8bod8P' " 
    </pre>
        <pre class="harry" tabindex="-1">
        .oooooo.                                 .o8       oooo                             
       d8P'  `Y8b                               "888       `888                             
      888            .oooo.   ooo. .oo.  .oo.    888oooo.   888   .ooooo.  oooo d8b  .oooo.o
      888           `P  )88b  `888P"Y88bP"Y88b   d88' `88b  888  d88' `88b `888""8P d88(  "8
      888     ooooo  .oP"888   888   888   888   888   888  888  888ooo888  888     `"Y88b. 
      `88.    .88'  d8(  888   888   888   888   888   888  888  888    .o  888     o.  )88b
       `Y8bood8P'   `Y888""8o o888o o888o o888o  `Y8bod8P' o888o `Y8bod8P' d888b    8""888P'
    </pre>
        <pre class="harry" tabindex="-1">
       .oooooo.                 o8o  oooo        .o8
      d8P'  `Y8b                `"'  `888       "888
     888           oooo  oooo  oooo   888   .oooo888
     888           `888  `888  `888   888  d88' `888
     888     ooooo  888   888   888   888  888   888
     `88.    .88'   888   888   888   888  888   888
      `Y8bood8P'    `V88V"V8P' o888o o888o `Y8bod88P
    </pre>
    </div>
    <div class="flex flex-col gap-8 items-center">
        <p>Making small bets is hard—don’t do it alone</p>
        <p class="text-gray-300">
            A small, private community of founders & indie hackers making small
            bets
        </p>

        <Dialog.Root>
            <Dialog.Trigger class={buttonVariants({ variant: "outline" })}>
                Apply
            </Dialog.Trigger>
            <Dialog.Content class="sm:max-w-[425px]">
                <Dialog.Header>
                    <Dialog.Title>Join The Gamblers Guild</Dialog.Title>
                    <Dialog.Description>
                        We're a private but inclusive group. If you'd like to
                        join, send through your details and we'll reach out.
                    </Dialog.Description>
                </Dialog.Header>
                <form
                    action="https://api.sheetmonkey.io/form/eKNhm9DsCrqH4RLzp5QZX"
                    method="post"
                    class="grid gap-4 py-4"
                >
                    <div class="grid grid-cols-4 items-center gap-4">
                        <Label class="text-right">Twitter/X</Label>
                        <Input
                            id="username"
                            class="col-span-3"
                            name="Twitter"
                            required
                        />
                    </div>
                    <div class="grid grid-cols-4 items-center gap-4">
                        <Label class="text-right">Email</Label>
                        <Input
                            id="email"
                            name="Email"
                            class="col-span-3"
                            type="email"
                            required
                        />
                    </div>
                    <input
                        type="hidden"
                        name="Created"
                        value="x-sheetmonkey-current-date-time"
                    />

                    <Dialog.Footer>
                        <!-- <input type="submit" value="Sign Up" /> -->
                        <Button type="submit" value="Sign Up">Submit</Button>
                        <!-- <Button type="submit">Save changes</Button> -->
                    </Dialog.Footer>
                </form>
            </Dialog.Content>
        </Dialog.Root>
    </div>

    <div
        class="flex flex-col max-w-sm md:flex-row gap-8 justify-center md:max-w-screen-md items-center"
    >
        <div class="flex flex-col gap-4 items-center">
            <pre
                style="white-space: pre;
  font-family: monospace;
  font-size: 3px;
  line-height: 3px;
  letter-spacing: unset;
  transform: unset;
  overflow-y: hidden;">                                                                                          
             AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA                     
           AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA                  
          AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA                 
        AAAAAAAAA AAAAAAAAA AAAAAAAAA AAAAAAAAAAAAAAAAAAAA                 
     AAAAAAAAAA     AAAAA     AAAAA     AAAAAAAAAAAAAAAAAA                 
      AAAAAAAAAA   AAAAAAA   AAAAAAA   AAAAAAAAAAAAAAAAAAA                 
          AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA                 
           AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA                  
            AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA                    
                                                                           
                                                                           
                  AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA               
                AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA             
               AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA            
            AAAAAAAAA   AAAAAAA   AAAAAAA   AAAAAAA   AAAAAAAAA            
          AAAAAAAAAA     AAAAA     AAAAA     AAAAA     AAAAAAAA            
            AAAAAAAAA   AAAAAAA   AAAAAAA   AAAAAAA   AAAAAAAAA            
               AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA            
                AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA             
                  AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA                
                                                                           
                                                                           
                      AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA          
                     AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA        
                    AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA       
                AAAAAAAAAA   AAAAAAA   AAAAAAAAAAAAAAAAAAAAAAAAAAAAA       
               AAAAAAAAAA     AAAAA     AAAAAAAAAAAAAAAAAAAAAAAAAAAA       
                  AAAAAAAAA AAAAAAAAA AAAAAAAAAAAAAAAAAAAAAAAAAAAAAA       
                    AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA       
                     AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA        
                       AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA           
</pre>
            <p>⚀ Forum</p>
            <p class="text-gray-300">
                A message board for weekly check-ins and long-form discussions
            </p>
        </div>
        <div class="flex flex-col gap-4 items-center">
            <pre
                style="white-space: pre;
  font-family: monospace;
  font-size: 3px;
  line-height: 3px;
  letter-spacing: unset;
  transform: unset;
  overflow-y: hidden;">                                                                                          
                         AAAAA               AAAAA                         
                  AAAAAAAAAAAAA             AAAAAAAAAAAAA                  
              AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA              
            AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA            
          AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA          
         AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA         
         AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA         
        AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA        
       AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA       
      AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA      
      AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA      
     AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA     
     AAAAAAAAAAAAAAAAAAAA     AAAAAAAAAAAAAAA     AAAAAAAAAAAAAAAAAAAA     
    AAAAAAAAAAAAAAAAAAAA       AAAAAAAAAAAAA       AAAAAAAAAAAAAAAAAAAA    
    AAAAAAAAAAAAAAAAAAA         AAAAAAAAAAA         AAAAAAAAAAAAAAAAAAA    
    AAAAAAAAAAAAAAAAAAA         AAAAAAAAAAA         AAAAAAAAAAAAAAAAAAA    
   AAAAAAAAAAAAAAAAAAAA         AAAAAAAAAAA         AAAAAAAAAAAAAAAAAAAA   
   AAAAAAAAAAAAAAAAAAAA         AAAAAAAAAAA         AAAAAAAAAAAAAAAAAAAA   
   AAAAAAAAAAAAAAAAAAAAA       AAAAAAAAAAAAA       AAAAAAAAAAAAAAAAAAAAA   
  AAAAAAAAAAAAAAAAAAAAAAAA   AAAAAAAAAAAAAAAAA   AAAAAAAAAAAAAAAAAAAAAAAA  
  AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA  
  AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA  
  AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA  
   AAAAAAAAAAAAAAAA       AAAAAAAAAAAAAAAAAAAAAAA       AAAAAAAAAAAAAAAA   
    AAAAAAAAAAAAAAAA                                   AAAAAAAAAAAAAAAA    
      AAAAAAAAAAAAAAAA                              AAAAAAAAAAAAAAAAA      
        AAAAAAAAAAAAAAAAAA                       AAAAAAAAAAAAAAAAA         
            AAAAAAAAAAAAA                         AAAAAAAAAAAAA            
                   AAAA                             AAAA                   
</pre>
            <p>⚁ Discord</p>
            <p class="text-gray-300">
                A Discord server for feedback and help requests
            </p>
        </div>
        <div class="flex flex-col gap-4 items-center">
            <pre
                style="white-space: pre;
  font-family: monospace;
  font-size: 3px;
  line-height: 3px;
  letter-spacing: unset;
  transform: unset;
  overflow-y: hidden;">                                                                                          
      AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA      
        AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA        
  AA      AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA      AA  
  AAAA      AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA      AAAA  
  AAAAAA      AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA      AAAAAA  
  AAAAAAAA      AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA      AAAAAAAA  
  AAAAAAAAAA      AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA      AAAAAAAAAA  
  AAAAAAAAAAAA      AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA      AAAAAAAAAAAA  
  AAAAAAAAAAAAAA      AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA      AAAAAAAAAAAAAA  
  AAAAAAAAAAAAAAAA      AAAAAAAAAAAAAAAAAAAAAAAAAAA      AAAAAAAAAAAAAAAA  
  AAAAAAAAAAAAAAAAAA      AAAAAAAAAAAAAAAAAAAAAAA      AAAAAAAAAAAAAAAAAA  
  AAAAAAAAAAAAAAAAAAAA      AAAAAAAAAAAAAAAAAAA      AAAAAAAAAAAAAAAAAAAA  
  AAAAAAAAAAAAAAAAAAAA        AAAAAAAAAAAAAAA        AAAAAAAAAAAAAAAAAAAA  
  AAAAAAAAAAAAAAAAAA            AAAAAAAAAAA            AAAAAAAAAAAAAAAAAA  
  AAAAAAAAAAAAAAAA      AAAA      AAAAAAA      AAAA      AAAAAAAAAAAAAAAA  
  AAAAAAAAAAAAAA       AAAAAA                 AAAAAA       AAAAAAAAAAAAAA  
  AAAAAAAAAAAAA      AAAAAAAAAA             AAAAAAAAAA      AAAAAAAAAAAAA  
  AAAAAAAAAAA      AAAAAAAAAAAAAAAA     AAAAAAAAAAAAAAAA      AAAAAAAAAAA  
  AAAAAAAAA      AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA      AAAAAAAAA  
  AAAAAAA      AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA      AAAAAAA  
  AAAAA      AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA      AAAAA  
  AAA       AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA       AAA  
  AA      AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA      AA  
        AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA        
      AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA      
</pre>
            <p>⚂ Email</p>
            <p class="text-gray-300">
                A weekly email round-up to highlight achievements
            </p>
        </div>
    </div>
    <div class="flex flex-col gap-2">
        <p>⚀ ⚁ ⚂ ⚃ ⚄ ⚅</p>
        <p class="text-gray-300">
            Audentes Fortuna Iuvat // Fortune favors the bold
        </p>
    </div>
</div>
