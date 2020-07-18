1) What are Channels and Kernels (according to EVA)?

Channels: Channels are Similar Feature Bags: We can think of channels as container of specfic feature type.
for example, characters could be channels in text, which combined togather makes a word, same set of charchatar combined in different way result to a different word (with different meaning)

Kernels : Feature Extractor: kernels are local spatial feature extractor, which can help us extract any specific features. 
key point with respect CNN are that we dont need to design this kernels, it converges to specific kernel based on the loss minimiztion using back propagation algorithm. therefore it converges to kernels which are useful in identifying particular object/pattern in image. 

for vertical kernel 
https://docs.google.com/spreadsheets/d/1DP-cOHGUbiSUn_jnpL4IWll__95Z5W_W67Es71nRuH0/edit?usp=sharingif 

we try to visualize an angle would be something like above. when a given filter is applied, it just captures value change in one direction.  In the above image look at leftmost top corner  3 X 3, elementwise multiplying this by given kernel/filter, we get -2. If we look at rightmost top corner do the same operation we get 0. So the value will be most negative when there is a transition/change in numeric value in rows(this is a little bit confusing, when we say vertical it means a change in the x-direction) 

Why should we (nearly) always use 3x3 kernels?
We can get the receptive field of all odd kernel(5x5,7x7 etc) using 3x3 kernels multiple times. 3x3 kernels are less memory itensive than their counterpart. 
for example: 5x5 kernel has 25 parmeters, using 3x3 twice can get same receptive field, but with 18 paramters only. 

NVIDIA GPU are accelerated for 3x3 kernels, therefore 3x3 computation work relatively faster too.


How many times to we need to perform 3x3 convolutions operations to reach close to 1x1 from 199x199 (type each layer output like 199x199 > 197x197...)
100

199x199 > 197x197 > 195x195 > 193x193 > 191x191 > 189x189 > 187x187 > 185x185 > 183x183 > 181x181 > 179x179 > 177x177 > 175x175 > 173x173 > 171x171 > 169x169 > 167x167 > 165x165 > 163x163 > 161x161 > 159x159 > 157x157 > 155x155 > 153x153 > 151x151 > 149x149 > 147x147 > 145x145 > 143x143 > 141x141 > 139x139 > 137x137 > 135x135 > 133x133 > 131x131 > 129x129 > 127x127 > 125x125 > 123x123 > 121x121 > 119x119 > 117x117 > 115x115 > 113x113 > 111x111 > 109x109 > 107x107 > 105x105 > 103x103 > 101x101 > 99x99 > 97x97 > 95x95 > 93x93 > 91x91 > 89x89 > 87x87 > 85x85 > 83x83 > 81x81 > 79x79 > 77x77 > 75x75 > 73x73 > 71x71 > 69x69 > 67x67 > 65x65 > 63x63 > 61x61 > 59x59 > 57x57 > 55x55 > 53x53 > 51x51 > 49x49 > 47x47 > 45x45 > 43x43 > 41x41 > 39x39 > 37x37 > 35x35 > 33x33 > 31x31 > 29x29 > 27x27 > 25x25 > 23x23 > 21x21 > 19x19 > 17x17 > 15x15 > 13x13 > 11x11 > 9x9 > 7x7 > 5x5 > 3x3 > 1x1 


How are kernels initialized? 
Kernels are intialized with random numbers, mostly between the range 0 to 1 

What happens during the training of a DNN?
while training a neural network,it(training) try to find optimal wights that would match an input to the desired output. for this it uses gradient of difference of ouput of the network and actual label, this gradient help in figuring out, how much addition or substraction is required from weights to find optimal wieghts iteratively (epoch). 
