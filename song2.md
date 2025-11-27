//Dreamrave Glitch - Witch House

setcps(135/60/4)

stack(
  s("bd*4, ~ sd:2, hh*8")
    .bank("RolandTR909")
    .room(0.6) 
    .shape(0.5)
    .gain(0.8),

  note("d2*4 f2*4 c2*4 g2*4")
    .s("supersaw")
    .lpf(900)
    .lpq(5)  
    .dist(0.3)
    .gain(0.7),

  note("<[d3,f3,a3] [f3,a3,c4] [c3,e3,g3] [g3,b3,d4]>")
    .s("superpwm")
    .attack(0.1)
    .release(1)
    .lpf(2500)
    .room(0.9) 
    .gain(0.45),

  note("[<a3 c4> a3 g3 e3] [c4 a3 g3 e3]")
    .s("sawtooth")
    .lpf(3000)
    .dist(0.8) 
    .chop(2)   
    .delay(0.5)
    .delaytime(0.125)
    .room(0.5) 
    .gain(0.65)
    .pan(sine.range(0.4, 0.6).slow(2))
)

const energia = slider(4700, 100, 8000, 100) 
const caos = slider(32, 1, 32, 1)            

stack(

  s("breaks:11")
    .slice(16, "0..15") 
    .ply(caos)         
    .lpf(energia)      
    .gain(1.5)
    ._scope({width: 800, height: 100}),

  // CAMADA 2: Melodia (Retângulos/Notas)
  // Os retângulos coloridos aparecem sozinhos quando você usa 'note'
  note("c3 [e3 g3] a3 [c4 b3]")
    .s("sawtooth")
    .lpf(energia) // O mesmo slider controla a melodia também
    .lpq(5)
    .delay(0.5)
    .gain(0.6)
)