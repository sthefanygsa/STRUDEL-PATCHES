//Rock Gótico - Alternativo

setCps(105/60/4)

const wall_intensity = slider(1, 0.1, 1, 0.05)

stack(

  s("bd*2 [~ sd:3]").bank("Rock") 
    .room(0.9)
    .gain(1.2)
    ._scope(), 
  note("c2*2 d2*2 f2*2 g2*2")
    .s("pulse")
    .distort(0.4)
    .lpf(300).lpq(1)
    .gain(0.8)
    .pianoroll(),

  note("c3 e4 g4 b4")
    .scale("c:dorian")
    .s("sawtooth")
    .distort(wall_intensity) 
    .room(1).roomsize(12) 
    .vibrato(0.1) 
    .slow(2) 
    .gain(0.9),

  note("c4*4 f4*4 g4*4 c4*4")
    .s("superpwm")
    .release(4) 
    .lpf(4000)
    .room(0.7)
    .gain(0.4)
)