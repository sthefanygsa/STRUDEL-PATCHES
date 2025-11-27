//Chiptune - Música 8-Bit

setCps(126/60/4)

stack(
  note("e4*2 e4*2 ~ e4*2 c4*2 e4*2 g4*4 ~ g3*4")
    .s("square")
    .gain(0.9)
    .pianoroll(), 

  s("bd:3*2 hh:3 [sd:4*2] hh:3*2") 
    .bank("RolandTR909")
    .delay(0.2) 
    .gain(0.7)
    ._scope(), 
  
  note("c3*4 g2*4 e2*4 a2*4")
    .s("pulse")
    .lpf(400) 
    .gain(0.6)
)