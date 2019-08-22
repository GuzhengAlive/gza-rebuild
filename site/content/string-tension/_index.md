---
title: Understanding String Tension
image: /img/white-background.jpeg
sections:
  - subsection:
      - subsectiontext: "Guzheng sellers often caution against using the wrong string in the wrong location on your instrument. “Things get too tight” they say “the strings will snap”. Okay, sure, we’ve all seen or heard of a string snapping, and most everyone will snap a string themselves at some point. But what kind of numbers are we talking about? I investigated and it turns out: a lot. A typical guzheng holds around 800 pounds of force on its strings (360kg)!  That’s like a group of people just standing on your instrument. That’s huge! \r\n\n\r\n\nI also investigated how much tension increases when you force a string too high. Well - A normal #2 string tuned to B5 would experience a tension of around 15 pounds (7 kg). But push that just two strings higher, to D6, and it sits at 20 pounds. That’s a 30% increase! E6 on the same string would demand 25 pounds, or 60% beyond design!\r\n\n\r\n\nThe bass strings are even scarier. A happy #21 string is already at ~60 pounds force (26kg). To push that two notes higher to G2 without moving the bridge you would need 120 POUNDS of force on that string.\r\n\n\r\n\nThis is why tuning distances and strings are important. Explore below to see the math of how I did it."
  - heading: The Setup
    subsection:
      - subsectiontext: >-
          We need math and we need measurements. The math for this comes from
          the [Mersenne-Taylor
          formula](https://pianotuninginyork.blogspot.com/2016/11/feeling-tension-2-calculating-tension.html):
      - caption: ''
        image: /img/taylor.png
        subsectiontext: "F = frequency (such as 440 Hz)\r\n\nL = The length of the string that is vibrating\r\n\nT = tension\r\n\nand µ = mass per unit length."
        target: Taylor
  - heading: Rearrange the Equation
    subsection:
      - subsectiontext: >-
          We want to get T, tension, by itself and everything else on the other
          side of the equals sign. Doing some quick algebra we get:
      - image: /img/tension.png
        subsectiontext: "Now, the length we can get from the [tuning charts](/guzheng-tuning). The frequency we can look up from a reference such as [VibrationData](http://www.vibrationdata.com/tutorials2/piano.pdf).  That leaves that funny looking µ.\r\n\nµ is Mass per length, which is another way of saying (surface area) x (density):"
        target: Tension
      - image: /img/mass-length-plain.png
        subsectiontext: >-
          If our strings are made only of drawn wire as used to be the case, we
          can use an equation like this:
        target: MassLengthPlain
      - image: /img/mass-length.png
        subsectiontext: "The first three terms are the surface area of the cross section of the wire, assuming it is a perfect circle.\r\n\n\rπ = the constant pi, 3.14159….\r\n\nd = diameter of the string, measured from the steel wire in question using calipers. Then:\r\n\nρ = density of the material. If we are just looking at steel-string guzheng then ~7.8 g/cm3 works for steel.\r\n\nUnfortunately modern guzheng use multi-layered, multi-material strings. The core is steel, then sometimes wound in copper, then wound in 2 layers of nylon thread or silk, and then wound in thicker nylon “wire”. So, we need to get the mass-per-unit-length of each of the materials, then combine them into one value. To get the mass per unit length, we need surface area for each."
        target: MassLength
  - heading: Calculate Mass per Length using Surface Area
    subsection:
      - subsectiontext: >-
          We need surface area for the steel, copper, and then the nylon and
          thread.
      - subheading: Steel
        subsectiontext: >-
          The above equation works for the steel core, so that’s
          straightforward. Unwinding the guzheng strings I measured the steel
          core and wrote it down.
      - image: /img/mass-length-steel.png
        subsectiontext: 'The density is for steel, 7.8 g/cm3'
        target: MassLengthSteel
      - subheading: Copper
        subsectiontext: >-
          I measured the diameter of the copper winding directly, but sometimes
          it is ribbon and sometimes, round wire. To keep the math reasonable I
          assumed it was always perfectly round wire. Sine the copper is wound
          around the steel core and is a constant diameter we can treat its
          cross section like a ring:
      - image: /img/m-l-ring.png
        subsectiontext: "R = the outer radius of the ring (steel + copper)\r\n\nr = the inner radius of the ring (steel)\r\n\nρ = density of copper. I used an approximate density for a copper alloy, 8.8g/cm3, because copper alloys tend to be cheaper than pure copper."
        target: mlring
      - caption: Outer radius for copper “ring”.
        image: /img/ring-outer-copper.png
        subsectiontext: ''
        target: RingOuterCopper
      - caption: Inner radius for copper “ring”.
        image: /img/ring-inner-steel.png
        target: RingInnerSteel
      - subheading: Nylon and Thread
        subsectiontext: >-
          Here I have to make another assumption - that the nylon wrapping and
          thread have the same density, and that they make up the rest of the
          diameter of the string. We again need to do the ring equation, but
          this time we’re using different values for the radii.
      - caption: >-
          Outer radius for the nylon ring is gotten from the total diameter of
          the string.
        image: /img/ring-outer-nylon.png
        target: RingOuterNylon
      - caption: >-
          The inner radius of the nylon ring is the distance taken up by the
          metals.
        image: /img/ring-inner-metals.png
        subsectiontext: "The inner radius is made of half the steel core diameter and the whole diameter of the cop\\per - because the copper winds around both sides of the core.\r\n\nPut these into the earlier mass per unit length for rings, and use the density of nylon, ~ 1g/cm3. You should now have three mass-per-unit-lengths, one for each material."
        target: RingInnerMetals
      - caption: Sum the three mass per length values together.
        image: /img/m-l-3-materials.png
        subsectiontext: >-
          Sum the values together and now you have the mass per length for a
          given section of modern guzheng wire.
        target: ml3materials
  - heading: Find the Tension
    subsection:
      - subsectiontext: >-
          Now we can bring the mass per length value back into the Tension
          equation.
      - caption: Final Tension equation.
        image: /img/final-tension.png
        subsectiontext: "Remember, \r\n\n\r\n\nL = the length of the string that vibrates. That’s only the distance between the tip of the right fixed bridge and the movable bridge for that string. We don’t factor in the left side of the instrument.\r\n\n\r\n\nF = the frequency or note that the string emits.\r\n\n\r\n\nRun this equation for each of the 21 strings and you get a tension in g/s2, or dynes. Convert that to pounds-force or Kilograms-force and you get: around 800 pounds force!"
        target: FinalTension
---

