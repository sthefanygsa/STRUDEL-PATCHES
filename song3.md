//Darkwave - EBM

setcps(133/60/4)

stack(
  s("bd sd:1")
    .bank("RolandTR909")
    .shape(0.4),

  s("~ hh*2")
    .bank("RolandTR909")
    .gain(0.8),

  note("a1*4 f1*4 c2*4 g1*4")
    .s("supersaw")
    .lpf(600)
    .lpq(3)  
    .gain(0.7),

  note("[<a3 c4> a3 g3 e3] [c4 a3 g3 e3]")
    .s("sawtooth")
    .lpf(2500)
    .dist(0.6) 
    .delay(0.5)
    .delaytime(0.125)
    .delayfeedback(0.6)
    .room(0.5)
    .gain(0.6)
)