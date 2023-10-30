<script>
    import { Button, buttonVariants } from "$lib/components/ui/button";
    import * as Dialog from "$lib/components/ui/dialog";
    import { Input } from "$lib/components/ui/input";
    import { Label } from "$lib/components/ui/label";
    import Tablerow from "../lib/components/ui/Tablerow.svelte";

    import { gsap } from "gsap";
    import { onMount } from "svelte";

    onMount(() => {
        //turn up the repeatDelay to make the glitch less frequent
        var tl = gsap.timeline({ repeat: -1, repeatDelay: 8 });
        //turn up the skewX to make the glitch more intense
        tl.to(".glitch", 0.1, { skewX: 30, ease: "power3.inOut" })
            .to(".glitch", 0.04, { skewX: 0, x: 20, ease: "power2.inOut" })
            .to(".glitch", 0.04, { opacity: 0 })
            .to(".glitch", 0.04, { opacity: 1 })
            .to(".glitch", 0.04, { x: -20 })
            .to(".glitch", 0.04, { x: 0 })
            .add("split", 0)
            .to(".top", 0.5, { x: -60, ease: "power3.inOut" }, "split")
            .to(".bottom", 0.5, { x: 60, ease: "power3.in" }, "split");
    });

    let members = [
        { name: "Akira", twitter: "akirathedev", joinDate: "30/10/2023" },
        {
            name: "Charlie Coppinger",
            twitter: "thecoppinger",
            joinDate: "30/10/2023",
        },
    ];
</script>

<div class="flex flex-col gap-24 items-center text-center px-8 py-8">
    <div class="flex flex-col gap-12 items-center">
        <div class="dice-wrapper translate-x-20">
            <pre
                class="glitch dice top"
                aria-hidden="true"
                tabindex="-1"
                id="output"
                style="white-space: pre;
                    font-family: monospace;
                    font-size: 6px;
                    line-height: 6px;
                    letter-spacing: unset;
                    transform: unset;
                    overflow-y: hidden;
                    filter:drop-shadow(1px 1px 10px rgba(20, 255,0))
">   
                                                                                     
                                                                                
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
</pre>
            <pre
                class="glitch top harry harry-glowing"
                aria-hidden="true"
                tabindex="-1"
                id="output">
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
        </div>
        <div class="flex flex-col md:flex-row">
            <p class="sr-only">The Gamblers Guild</p>
            <pre aria-hidden="true" class=" harry" tabindex="-1">
ooooooooooooo oooo                  
8'   888   `8 `888                  
     888       888 .oo.    .ooooo.  
     888       888P"Y88b  d88' `88b 
     888       888   888  888ooo888 
     888       888   888  888    .o 
    o888o     o888o o888o `Y8bod8P' 
    </pre>
            <pre aria-hidden="true" class=" harry" tabindex="-1">
        .oooooo.                                 .o8       oooo                               
       d8P'  `Y8b                               "888       `888                               
      888            .oooo.   ooo. .oo.  .oo.    888oooo.   888   .ooooo.  oooo d8b  .oooo.o  
      888           `P  )88b  `888P"Y88bP"Y88b   d88' `88b  888  d88' `88b `888""8P d88(  "8  
      888     ooooo  .oP"888   888   888   888   888   888  888  888ooo888  888     `"Y88b.   
      `88.    .88'  d8(  888   888   888   888   888   888  888  888    .o  888     o.  )88b  
       `Y8bood8P'   `Y888""8o o888o o888o o888o  `Y8bod8P' o888o `Y8bod8P' d888b    8""888P'  
    </pre>
            <pre aria-hidden="true" class=" harry" tabindex="-1">
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
            <p>
                Building stuff can be lonely, overwhelming and tiring, so we're
                doing it together.
            </p>
            <p class="text-gray-300">
                A small, private community of founders & indie hackers making
                small bets and supporting each other.
            </p>

            <Dialog.Root>
                <Dialog.Trigger class={buttonVariants({ variant: "outline" })}>
                    Apply
                </Dialog.Trigger>
                <Dialog.Content class="sm:max-w-[425px]">
                    <Dialog.Header>
                        <Dialog.Title>Join The Gamblers Guild</Dialog.Title>
                        <Dialog.Description>
                            We're a private but inclusive group. If you'd like
                            to join, send through your details and we'll reach
                            out.
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
                            <Button type="submit" value="Sign Up">Submit</Button
                            >
                        </Dialog.Footer>
                    </form>
                </Dialog.Content>
            </Dialog.Root>
        </div>
    </div>

    <div
        class="flex flex-col max-w-sm md:flex-row gap-8 justify-center md:max-w-screen-lg items-center mt-8"
    >
        <div class="flex flex-col gap-4 items-center w-full">
            <pre
                aria-hidden="true"
                class="harry-glowing"
                style="white-space: pre;
  font-family: monospace;
  font-size: 1px;
  line-height: 1px;
  letter-spacing: unset;
  transform: unset;
  overflow-y: hidden;">                                                                                          
             ........................................:.....::::::::::::::::::::::::::::::::::::::::::::::::::::::             
          ...:;+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx++;:           
         .:;+xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX++          
         ;xXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX$$XX$$$$$$$$$$$$$$$$$$$$$$$$$XX          
         xXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$XX         
         XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$X         
         XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX$XXX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$X         
         XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX$X$XX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$X         
         XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$X         
         XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX$$XX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$X         
         XXX$XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX$XX$X$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$X         
         XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$X         
         XX$$XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$X         
         XX$$XXXXXXXXXXXXXX$X+::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::+X$$$$$$$$$$$$$$$$$$X         
         XX$$XXXXXXXXXXXXXX$+....................................................................+$$$$$$$$$$$$$$$$$$X         
         XX$$XXXXXXXXXXXXX$$x....................................................................+$$$$$$$$$$$$$$$$$$X         
         XX$$XXXXXXXXXXXXX$$x:..................................................................:+$$$$$$$$$$$$$$$$$$X         
         XX$$XXXXXXXXXXX$X$$x:..................................................................:+$$$$$$$$$$$$$$$$$$X         
         XX$$$XXXXXXXXXX$X$$x:..................................................................:x$$$$$$$$$$$$$$$$$$X         
         XX$$XXXXXXXXXXXX$$X$XXxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxXX$$$$$$$$$$$$$$$$$$$X         
         XX$$$XXXXXXXXXXXXXXX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$XX         
         XX$$$XXXXXXXXXXXXXXX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$X         
         XX$$$XXXXXXXXXXXXXXX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$X         
         XX$$XXXXXXXXXXXXXXXX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$X         
         XX$$XXXXXXXXXXXXXXXXXXxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxXX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$X         
         XX$$XXXXXXXXXXXXXXXx:...................................................;$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$X         
         XX$$XXXXXXXXXXXXX$$x....................................................:X$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$X         
         XXX$XXXXXXXXXXXXX$$x:...................................................;$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$X         
         XXXXXXXXXXXXXXXXXX$x:...................................................;$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$XX         
         XX$$XXXXXXXXXXXXXX$x:...................................................;$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$X         
         XX$$XXXXXXXXXXXXX$$X+::::::::::::::::::::::::::::::::::::::::::::::::::;x$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$XX         
         XX$$$XXXXXXXXXXXXXX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$XX         
         XX$$XXXXXXXXXXXXXXXX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$XX         
         XX$$$XXXXXXXXXXXXXXX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$XX         
         XX$$$$XXXXXXXXXXXXXX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$XX         
         XX$$$X$$$$XXXXXXXXXXX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$X         
         XX$$$X$XXXXXXXXXXXXXX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$XX         
         XX$$$$$$$$$XXXXXXXXXX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$X         
         XX$$$$$X$$XX$$XXXXXXXX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$X         
         XX$$$$$$$$$$$$XXXXXXX$$$$$$$$$$$$$$$$$$$$$$$$$$$$X$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$X         
         XX$$$$$$$$$$$XXXXXXXXXX$$$$$$$$$$$$$$$XXXXXXXXXXXXXXXXXXXXXX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$X          
         XX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$XX$$XXXXX$XX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$XX          
          XX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$XXXX$$X$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$X           
            $XX$$$$$$$$$$$$$$$$$$$$$$$$$$$$XXXXXXX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$XXXXXXXX$$$$$$$$$$$$$$$$$$$$$X             
                                 $$$$$$$XXXXXXXXXXX$$$$$$$$$$$$$XX                                                            
                                 X$$$$$$XXXXXXXXXX$$$$$$$$$$$$XX                                                              
                                 X$$$$$XXXXXXXXX$$$$$$$$$$$XX                                                                 
                                 X$$$$$XXXXXXXX$$$$$$$$$$$X                                                                   
                                  X$$$XXXXXXXX$$$$$$$$$$XX                                                                    
                                  X$$$XXXXXX$$$$$$$$$$X$                                                                      
                                  X$$$XXXXXX$$$$$$$$XX                                                                        
                                  XX$XXXXX$$$$$$$$XX                                                                          
                                  XXXXXXXX$$$$$$XX                                                                            
                                 xXXXXXX$$$$$$$XX                                                                             
                                 xXXXX$$$$$$$XX                                                                               
                                  XX$$$$$$$XX                                                                                 
                                   X$$$$$$X                                                                                   
                                     X$$$                                                                                     

</pre>
            <p>⚀ Forum</p>
            <p class="text-gray-300">
                A message board for weekly check-ins and long-form discussions
            </p>
        </div>
        <div class="flex flex-col gap-4 items-center w-full">
            <pre
                aria-hidden="true"
                class="harry-glowing"
                style="white-space: pre;
  font-family: monospace;
  font-size: 1px;
  line-height: 1px;
  letter-spacing: unset;
  transform: unset;
  overflow-y: hidden;">                                                                                          
                                      ...........                            ...........                                      
                                 .................                          ..................                                
                             ......................                        ......:::::.::::::....                             
                          ...............::::::::..............................:::::::::::::::::::...                         
                       .............:::::::::::::::...........................:::::::::::::::::::::::...                      
                     ..........:::::::::::::::::::::........................::::::;;;;;;;;;;;;;;;:::;;::..                    
                   .........:::::::::::::::::::::::::::...............:::::::::;;;;;;;;;;;;;;;;;;;;;;;;;;::.                  
                  ........:::::::::::::;;;;;;;;;;;::::::::::::::::::::::::::;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;:.                 
                 ......::::::::::;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;++++++++++++++++;;;;;;;;;;                 
                 ...:::::::::;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;+++++++++++++++++++++++++;;;;;:                
                ...:::::::;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;++++++++++++++++++++++++++++++++++;;:               
               ..::::::;;;;;;;;;;;;;;;;;;;++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++;;              
              ..::::;;;;;;;;;;;;;;++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++;;:             
              ..:::;;;;;;;;;;;+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++;;             
             .::;;;;;;;;;;++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++;;            
            .::;;;;;;;;++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++;            
            .:;;;;;;;;++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++xx++xxxxxxxxxx+xxx++++++++++++;           
           .:;;;;;;;++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++xxxxxxxxxxxxxxxxxxxxxxxxx+++++++++++          
          ..:;;;;;+++++++++++++++++++++++++++++++++++++++++++++++++++++++++xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx++++++++         
          ::;;;;;+++++++++++++++++++++++++++xxxxxx+x+++++++++++++++++++xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx+x+++++         
         .:;;;;+++++++++++++++++++++++xxxx++;;;;;+xxxxxxxx+++++++++xxxxxxxxxx++;;;++xxxxxxxxxxxxxxxxxxxxxxxxxxxxxx+++         
         :;;;;++++++++++++++++++++xxxxxx+:.........:+xxxxxxxxxxxxxxxxxxxxxx;.........:xxxxxxxxxxxxxxxxxxxxxxxxxxxxx+++        
        .:;;;++++++++++++++++xxxxxxxxxx;.............;xxxxxxxxxxxxxxxxxxx;.............;xXxxxxxxxxxxxxxxxxxxxxxxxxx+++        
        :;;+++++++++++++xxxxxxxxxxxxxx;...............;xxxxxxxxxxxxxxxxx;...............;xXxxxxxxxxxxxxxxxxxxxxxxxxxxx+       
        ;;++++++++++xxxxxxxxxxxxxxxxx;.................+xxxxxxxxxxxxxxx+.................+XXxxxxxxxxxxxxxxxxxxxxxxxxxxxx      
       :;++++++++xxxxxxxxxxxxxxxxxxxx:.................;xXxxxxxxxxxxxxX:.................;XXXxxxxxxxxxxxxxxxxxxxxxxxxxxx      
      :;++++++xxxxxxxxxxxxxxxxxxxxxXx:.................;xXxxxxxxxxxxxXX:.................;XXXXxxxxxxxxxxxxxxxxxxxxxxxxxx      
      ;;++++xxxxxxxxxxxxxxxxxxxxxxxXX;.................+XXXxxxxxxxxxxXX;.................;XXXXXXxxxxxxxxxxxxxxxxxxxxxxxx      
      +++++xxxxxxxxxxxxxxxxxxxxxxxXXXx:...............:xXXXXXxxxxxxXXXXx:...............;x$XXXXXXXXXxxxxxxxxxxxxxxxxxxxxx     
      ++xxxxxxxxxxxxxxxxxxxxxxxxxXXXXXx:.............:xXXXXXXXXXXXXXXXXXx:.............:+XXXXXXXXXXXXXXXXXXXXXXxxxxxxxxxx     
     ++xxxxxxxxxxxxxxxxxxxxxXXXXXXXXXXXX;:..........;x$XXXXXXXXXXXXXXXXXXX;...........;xXXXXXXXXXXXXXXXXXXXXXXXXXXXxXXxXX     
     +xxxxxxxxxxxxXXXXXXXXXXXXXXXXXXXXXXXx+;:::::;+xXXXXXXXXXXXXXXXXXXXXXXXx+;:::::;+xXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX     
     xxxxxxxxxxXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXx    
     xxxxxxXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXx    
     xxXxXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX    
     xXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX    
     XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX    
     XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX    
     XXX$$XXXXXXXXXXXXXXXXXXXXX$$$$$XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX$$$$$$$$XXXXXXXXXXXXXXXXXXXX$$XX     
      XXX$$$$$XXXXXXXXXXXXXXXX$$$$$$$$$$$$XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX$$$$$$$$$$$$$XXXXXXXXXXXXXXX$$$$$$XXX     
        XXX$$$$$$$$XXXXXXXXXXXXX$$X $$$$$$$$$$$$$$XXXXXXXXXXXXXXXXXXXXXXXXXXX$$$$$$$$$$$$$$X$$$$$XXXXXXXXXXX$$$$$$$$XXX       
           xX$$$$$$$$$$$XXXXXXXX$$$++     X$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$     ;xX$$XXXXXXX$$$$$$$$$$$XXX          
             XXX$$$$$$$$$$$$XXXXXX$$XXxx+;     XXXXXXXXX$XX$$$$$$$$$$$$XXXXXXXXx    ;+xXXX$$XXXXXX$$$$$$$$$$$$$XXx            
                XXX$$$$$$$$$$$$XXXXXXX$$Xxx                                        +xX$XXXXXXXXX$$$$$$$$$$$$XXX               
                    XX$$$$$$$$$$$$XXXXXXXXX                                        X$XXXXXXX$$$$$$$$$$$$XXx                   
                       XXX$$$$$$$$$$$$$XXX                                          XX$$$$$$$$$$$$$$XXX                       
                             XXXXXXXXXXX                                              XXXXXXXXXX$X                            
</pre>
            <p>⚁ Discord</p>
            <p class="text-gray-300">
                A Discord server for quick feedback and help requests
            </p>
        </div>
        <div class="flex flex-col gap-4 items-center w-full">
            <pre
                aria-hidden="true"
                class="harry-glowing"
                style="white-space: pre;
  font-family: monospace;
  font-size: 1px;
  line-height: 1px;
  letter-spacing: unset;
  transform: unset;
  overflow-y: hidden;">
          xxx+xx;...........................................................................................;xXXXXXX          
        +xxxxxxx+;.........................................................................................;xXXXXXXXXX        
       xxxxxxxxxxxx+:...................................................................................:+XXXXXXXXXXXX        
      xxxxxxxxxxxxxxx+;...............................................................................;xXXXXXXXXXXXXXX        
      xxxxxxxxxxxxxxxxxx+:.........................................................................:+xXXXXXXXXXXXXXXXX        
      xxxxxxxxxxxxxxxxxxxXx+.....................................................................;XXXXXXXXXXXXXXXXXXXXX       
       xXxxxxxxxxxxxxxxxxxxXx+:...............................................................:+XXXXXXXXXXXXXXXXXXX$$$$       
       $$XXxXXXXXXXXXXXXXXXXXXXx;...........................................................;xXXXXXXXXXXXXXXXXXXXXX$$$$       
       $$$$$XXXXXXXXXXXXXXXXXXXXXXx:......................................................+XXXXXXXXXXXXXXXXXXXXXX$$$$$$       
       $$$$$$$$XXXXXXXXXXXXXXXXXXXXXx;.................................................;xXXXXXXXXXXXXXXXXXXXXX$$$$$$$$$       
       $$$$$$$$$$XXXXXXXXXXXXXXXXXXXXXXx;...........................................:+XXXXXXXXXXXXXXXXXXXXX$$$$$$$$$$$$       
       $$$$$$$$$$$$XXXXXXXXXXXXXXXXXXXXXXX+.......................................;xX$XXXXXXXXXXXXXXXXXX$$$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$$XXXXXXXXXXXXXXXXXXXXXXx;.................................:+XXXXXXXXXXXXXXXXXXX$$$XX$$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$X+xXXXXXXXXXXXXXXXXXXXXXXX+:............................;XXXXXXXXXXXXXXX$$$$$$$XX+;+$$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$x;;+xXXXXXXXXXXXXXXXXXXXXXXXx;.......................:+X$$XXXXXXX$X$$$$$$$$$$Xx+;::+$$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$x:::;;+xXXXXXXXXXXXXXXXXXXXXXXX+:..................;xX$$XX$$$$$$$$$$$$$$$$XX+;;::::+$$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$x:.::::;++XXXXXXXXXXXXXXXXXXXXXXXX;.............:xX$$X$$$$$$$$$$$$$$$$$$Xx;;::::::.+$$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+....::::;;+xXXXXXXXXXXXXXXXXXXXX$$X+:........;xX$$$$$$$$$$$$$$$$$$$$XX+;:::::.....;$$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+.......::::;;+XXX$XX$XXXX$$$$$$$$$$$XX;...:+X$$$$$$$$$$$$$$$$$$$$$Xx;;::::........;$$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+.........::::;;+xX$$$$$$$$$$$$$$$$$$$$$$XX$$$$$$$$$$$$$$$$$$$$$$X+;::::...........;$$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+............::::;;xXX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$Xx;;:::..............;$$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+..............::::;;+xX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$X+;::::................;X$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+.................::::;;xX$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$Xx;;:::...................;X$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+...................::::;;+xX$$$$$$$$$$$$$$$$$$$$$$$$$$X+;::::.....................;X$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+......................::::;;+X$$$$$$$$$$$$$$$$$$$$$Xx;;:::........................;X$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+........................::::;;+xX$$$$$$$$$$$$$$$$X+;::::..........................;X$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+...........................::::;;+X$$$$$$$$$$$Xx;;:::.............................;X$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+.............................:::::;+x$$$$$$$X+;::::...............................;X$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+................................::::;;xX$Xx;::::..................................;X$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+..................................::;;;;;:::::....................................;X$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+..................................::::............................................;X$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+.................................:................................................;X$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+..................................................................................;X$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+..................................................................................;X$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+..................................................................................;X$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+..................................................................................;X$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+..................................................................................;X$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+..................................................................................;X$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+..................................................................................;X$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+..................................................................................;X$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+..................................................................................;X$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+..................................................................................;X$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+..................................................................................;X$$$$$$$$$$$$$       
       $$$$$$$$$$$$$$+..................................................................................;X$$$$$$$$$$$$        
       $$$$$$$$$$$$$$+..................................................................................;X$$$$$$$$$$$$        
        $$$$$$$$$$$$$+..................................................................................;X$$$$$$$$$$$$        
         $$$$$$$$$$$$+..................................................................................:X$$$$$$$$$$          
            </pre>

            <p>⚂ Email</p>
            <p class="text-gray-300">
                A weekly email round-up to highlight achievements
            </p>
        </div>
    </div>
    <div class="flex flex-col gap-8">
        <div class="flex flex-col gap-4">
            <p>Founding Members</p>
            <p class="text-gray-300">⚀ ⚁ ⚂ ⚃ ⚄ ⚅</p>
        </div>
        <pre
            style="    white-space: pre;
    font-family: monospace;
    font-size: 3px;
    line-height: 3px;
    letter-spacing: unset;
    transform: unset;
    overflow-y: hidden;"
            class="harry-glowing">
            ;:::;;;+                        +;;::::::::::::::::;;                                                             
          :::...:::;;++                +++;;::..................:::::;                                                        
        ::..........::;;;;;;;;;;;;;;;;;+++;:.........................::::;                                                    
      ::...............::::::::::::;;;;++;:..............................:::;;;;                         +++;;;;;             
     :.........................::::;;;++;:....................................:::::::;               ++++;;:::...:.           
    ::..........................::::;++;:............................................:::;+      ++;;;;;;::..........          
   ::............................::;;+;:...............:::..............................::;;;;;;;;::.................:        
  ::.............................::;+;...............:;;;::;;;;::...........................:::........................       
  :..............................:;;:..............::;::.......:;;:::..................................................:      
 ::.............................::+;..............::;:............::;:::................................................:     
 ::..............................:+;:............::::................:;;::::............................................::    
;::..............................:;;;:........:::::....................::;;;:::..........................................::   
;:::..............................:;+;:::::::;;::.........................:;;;;:::::....................................::::  
;;::::::............................::;;;;;;;::..............................:;;;;;;:::::...............................::::  
+;;:::::::::....................................................................:;++;;;;;::::.........................::::::; 
++;;;;;;::::::::::::...............................................................:;+++;;;;::::.....................:::::::: 
 ++++;;;;;;;;;::::::::................................................................:;++++;;;:::........................::::
  x+++++++++;;;;;;;;::::.................................................................:;++++;;:::.....................:::;;
     +xx++++++++++;;;;::::..................................................................:;+++;;;::::..........:::::::;;;; 
        ++xx++++++++;;;::::....................................................................:;+++;;::::::::::::::::;;++++  
           xxxxx+++++;;;;::::....................................................................:;+++;;;;::::::::;;+++++     
             xxxxx+++++;;;:::::.........................................;;;:.......................:;+++++;;;;;;;++++         
               xxxx+++++;;;;:::::.........................................::::::...................::;++++++++++++            
                 xxxx+++++;;;;:::::.............................................::::...............::;;++xx+++++x             
                  xxxx++++++;;;;:::::..............................................:;;;:...........:::;++xxxxxx               
                    xxxx+++++;;;;::::::...............................................:;;+;;::....::::;;++xxxx                
                      xxxx+++++;;;;:::::.................................................:;+++;;::::;;;;;++x                  
                       xxxxx++++;;;;:::::......................::::::......................:;+++++;;;;;;;;++                  
                         xxxx+;:::;;;;:::::........................:;++;:....................:;+x+++;;;;;;++                  
                          ++;:.....:;;;:::::..........................:;++;::................::;+++++;;;;;+                   
                         x++;:......:;+;:::::............................:;+++;:.............::;;++x+++++;                    
                         xx++;:....::;+;;:::::........::...................:;+++;;:.........::;;++++x+++                      
                         xxx++;;:::;;+++;;;++;;;::::::;++;;::.................:;;+++;::::::;;;;+++++                          
                          xxxx++;;;;++x+++++;::...:::..:;;+++;;:.................:;+++++++++++++++++                          
                          xxxxx++++++xxx++;:........::...:::;;;;;;::................:;++xx++++++++x                           
                           xxxxx+++xxxx++;:.........:;;;;;:::..::;++;;:.............::;++xxxxxx+                              
                             xxxxxxxxx+++;::.......:;+;;::::::...::;;++;;;::......::;;+++++                                   
                                    x++++;;::.....:;+;:......:;++;;;;;::;;++;;;;;;;++++++++                                   
                                    x++++;;;:::::;++;:.......:;;:.....:::..::;;++++++++++x                                    
                                    ++++++;;;;;;;+++;........:;:........:.....::;+x+xx                                        
                                     x++++++;;;+++++;:.......:;.........;::::::;;                                             
                                        +++++++++++;;:::...:;;;........:++;;;;                                                
                                               ++++;;::::::;++;:......:;++                                                    
                                                +++;;:::::;;+++;::::::;;;                                                     
                                                 x++;;;:;;;;x+++;;;;;;++                                                      
                                                    ++;;;;    +++++++++                                                       
        </pre>
        <ul class="flex flex-col gap-4 max-w-screen-sm justify-between">
            <Tablerow />
            {#each members as member}
                <Tablerow {...member} />
            {/each}
        </ul>
    </div>
    <div class="flex flex-col gap-2">
        <p>⚀ ⚁ ⚂ ⚃ ⚄ ⚅</p>
        <p class="text-gray-300">
            Audentes Fortuna Iuvat // Fortune favors the bold
        </p>
    </div>
    <div class="flex gap-2">
        <p>Credits:</p>
        <p class="text-gray-300">
            Glitch animation by <a
                href="https://twitter.com/harry_webb98"
                target="_blank">Harry</a
            >
        </p>
    </div>
</div>
