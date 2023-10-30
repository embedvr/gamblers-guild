<script lang="ts">
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
</script>

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
		filter:drop-shadow(1px 1px 10px rgba(20, 255,0));">   
                                                                                     
                                                                                
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
    class="glitch top"
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
