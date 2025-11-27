//Synth-Pop - New Wave

setcps(118/60/4)

stack(
  s("bd [~ sd:3] bd [~ sd:3]")
    .bank("Linn")
    .shape(0.3)  
    .gain(0.9),

  s("hh*8")
    .bank("Linn")
    .gain(0.45)
    .pan(0.4),

  note("g1*2 as1*2 f1*2 c2*2") 
    .s("sawtooth")
    .lpf(600) 
    .lpq(2)
    .cut(1)  
    .gain(0.85),

  note("d4 ~ ~ c4 ~ ~ <as3 a3> ~")
    .s("square")
    .lpf(1800)
    .vibrato(1.5)
    .delay(0.4)
    .delaytime(0.375)
    .room(0.4)
    .gain(0.6),

  note("<g3 f3>")
    .s("sine")
    .attack(0.5)
    .release(1)
    .room(0.8)
    .gain(0.4)
)