# Water Resources

Here's a list of links and references to various pieces of research/games/systems which contain water rendering and could be of interest and inspiration!

If you know of an interesting example of that is missing from this list, please create an issue or pull request!

## Category Breakdown

We break down work by the following categories, we also make sure that any work which falls under multiple categories can be found under all of them.

  - [Animated Waves](#animated-waves)
    - [FFT](#fft)
    - [Gerstner Waves](#gerstner-waves)
    - [Wave Particles](#wave-particles)
  - [Dynamic Waves](#dynamic-waves)
    - [Eularian](#eularian-dynamic-waves)
    - [Lagrangian](#lagrangian-dynamic-waves)
    - [Hybrid](#hybrid-dynamic-waves)
    - [Other](#other-dynamic-waves)
  - [Meshing](#meshing)
  - [Foam](#foam)
  - [Flow](#flow)
  - [Libraries and Systems](#libraries-and-systems)
  - [Collations and Surveys](#collations-and-surveys)
  - [Wave Theory](#wave-theory)
  <!-- TODO
  - [3D Sims](#3d-sims)
    - [Eularian](#eularian-3d-sims)
    - [Lagrangian](#lagrangian-3d-sims)
    -->


## Animated Waves

### FFT
  - __[Simulating Ocean Water](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.131.5567&rep=rep1&type=pdf)__, Tessendorf, 2001

### Gerstner Waves
  - __[Simulating Ocean Water](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.131.5567&rep=rep1&type=pdf)__, Tessendorf, 2001
  - __[Water Technology of Uncharted](https://cgzoo.files.wordpress.com/2012/04/water-technology-of-uncharted-gdc-2012.pdf)__, Gonzalez-Ochoa & Holder, 2012: Gerstner Waves are used for large low-frequency waves in oceans.

### Other
  - __[Wave Particles](http://www.cemyuksel.com/research/waveparticles/)__, Yuksel, 2007: The foundation for the animated wave techniques used in Uncharted.
  - __[Water Technology of Uncharted](https://cgzoo.files.wordpress.com/2012/04/water-technology-of-uncharted-gdc-2012.pdf)__, Gonzalez-Ochoa & Holder, 2012: Wave particles are used to add high-frequency wave information to oceans.
  - __[Rendering Rapids in Uncharted 4](http://advances.realtimerendering.com/s2016/Rendering%20rapids%20in%20Uncharted%204.pptx)__, Gonzalez-Ochoa, 2016: Wave particles are scrolled in the direction of river flow to help render rapids.
  - __[Water Surface Wavelets](http://visualcomputing.ist.ac.at/publications/2018/WSW/)__, Jeschke et al., 2018: Can pre-bake steady-state of simulation grid and interpolate between states to get reflecting waves at static-boundary conditions without need for run-time dynamic wave sim.

## Dynamic Waves

### Eularian Dynamic Waves
  - __[Simulating Ocean Water](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.131.5567&rep=rep1&type=pdf)__, Tessendorf, 2001
  - __[Real-time Interactive Water Waves](http://www.dice.se/wp-content/uploads/2014/12/water-interaction-ottosson_bjorn.pdf)__, Ottosson
  - __[Dispersion Kernels for Water Wave Simulation](https://gmrv.es/Publications/2016/CMTKPO16/main.pdf)__, Canabal et al., 2016
  - __[Real-Time Large Scale Fluids for Games](https://pdfs.semanticscholar.org/a3c5/5aeda63895d846c38ae23e921cec7320f584.pdf)__, Kallin
  - __[Fast Water Simulation for Games Using Height Fields](http://matthias-mueller-fischer.ch/talks/GDC2008.pdf)__, Müller-Fischer, 2008
  - __[Real-Time Open Water Environments with Interacting Objects](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.162.2833&rep=rep1&type=pdf)__, Cords and Staadt, 2009: Real-Time Grid-Based solution using Finite Differences Method (FDM) with multiple sims, includes comparison with Wave Particles.
  - __[Water Surface Wavelets](http://visualcomputing.ist.ac.at/publications/2018/WSW/)__, Jeschke et al., 2018: Generalises theory behind Lagrangian `Water Wave Packets` and proposes a relatively performant Eularian alternative that is used to simulate water on a 4km x 4km grid with low frequency simulation - loss in detail comes from artifacting in dispersion as opposed to lower-frequency waves.

### Lagrangian Dynamic Waves
  - __[Wave Particles](http://www.cemyuksel.com/research/waveparticles/)__, Yuksel, 2007: Dynamic water surface waves represented using 2D lagrangian surface-sim where point particles are splatted to a texture and the convolved using a kernel that can create convincing trochoidal wave shapes.
  - __[Water Wave Packets](http://visualcomputing.ist.ac.at/publications/2017/WWP/)__, Jeschke & Wojtan, 2017: Wave packets used to represent the energy of groups of wave trains instead of individual wave crests - allows for more high-frequency information with smaller number of particles.

### Hybrid Dynamic Waves
  - __[Real-time Simulation of Large Bodies of Water with Small Scale Details](https://www.semanticscholar.org/paper/Real-time-Simulation-of-Large-Bodies-of-Water-with-Chentanez-M%C3%BCller/8b89fb1c664b742271e0f19a9efe8492f14074f5)__, Chentanez & Müller-Fischer, 2010. _[Video](https://www.youtube.com/watch?v=bojdpqi2l_o)_

### Other Dynamic Waves
  - __Interactive Simulation of Water Surfaces__, Gomez, 2000. Found in _Game Programming Gems_.

## Meshing
  - __[Water Technology of Uncharted](https://cgzoo.files.wordpress.com/2012/04/water-technology-of-uncharted-gdc-2012.pdf)__, Gonzalez-Ochoa & Holder, 2012

## Foam
  - __[Rendering Rapids in Uncharted 4](http://advances.realtimerendering.com/s2016/Rendering%20rapids%20in%20Uncharted%204.pptx)__, Gonzalez-Ochoa, 2016

## Flow
  - __[Water Technology of Uncharted](https://cgzoo.files.wordpress.com/2012/04/water-technology-of-uncharted-gdc-2012.pdf)__, Gonzalez-Ochoa & Holder, 2012: Normal-map scrolling technique used to render rivers in Uncharted: Drake's Fortune.
  - __[Rendering Rapids in Uncharted 4](http://advances.realtimerendering.com/s2016/Rendering%20rapids%20in%20Uncharted%204.pptx)__, Gonzalez-Ochoa, 2016: Much more advanced pipeline used than first Uncharted used to create convincing rapids with a multitude of techniques.

## Libraries and Systems
  - __[Hydrax](https://github.com/imperative/CommunityHydrax)__, Open-Source plugin for OGRE

## Collations and Surveys
  - __[VTP](http://vterrain.org/Water/)__
  - __[A survey of ocean simulation and rendering techniques in computer graphics](https://arxiv.org/pdf/1109.6494.pdf)__, Darles et al., 2011

## Wave Theory
  - __[What determines the speed of waves in water?](https://physics.stackexchange.com/questions/121327/what-determines-the-speed-of-waves-in-water/121330#121330)__, Physics Stackexchange: Longer wavelengths travel faster. For a swell, longest wavelengths arrive first.
  - __[Wind wave](https://en.wikipedia.org/wiki/Wind_wave)__, Wikipedia
  - __[Essentials of Oceanography](https://topex.ucsd.edu/ps/trujillo_waves.pdf)__, Thurman & Trujilo: Great text about water waves of all types.
  - __[Environmental Fluid Mechanics, Chapter 4: Waves](http://www.dartmouth.edu/~cushman/books/EFM/chap4.pdf)__, Cushman-Roisin, 2019: Nice chapter on water wave phenomena, shows pressure profile of wind travelling over and obstacle.

<!--
  - http://www-eaps.mit.edu/~rap/courses/12333_notes/dispersion.pdf : Useful notes on dispersive and non-dispersive waves.
  - https://thayer.dartmouth.edu/~d30345d/books/EFM/chap4.pdf : More notes on waves.
  - https://ccrma.stanford.edu/~jos/pasp/Dispersive_1D_Wave_Equation.html : Dispersive wave equation.
  - http://www.bu.edu/pasi-tsunami/files/2013/01/daytwo12.pdf : Dispersion does not apply to tsunamis.
  - https://pdfs.semanticscholar.org/c902/c4f2c61734cbf4ec7ee8b792ccb01644943d.pdf, Thuery: Detailed SWE description
  - http://kestrel.nmt.edu/~raymond/classes/ph332/notes/shallowgov/shallowgov.pdf, Using SWE for ocean on large scales
  - Three stages of how wind generates waves, with refs: https://www.wikiwaves.org/Ocean-Wave_Spectra
  - Miles - how energy is transferred from wind to wave: https://www.cambridge.org/core/journals/journal-of-fluid-mechanics/article/on-the-generation-of-surface-waves-by-shear-flows/40B503619B6D4571BEF3D31CB8925084
  - Realistic simulation of waves using wave spectra: https://hal.archives-ouvertes.fr/file/index/docid/307938/filename/frechot_realistic_simulation_of_ocean_surface_using_wave_spectra.pdf
  - Nice practical demo about testing different wave breakers: https://youtu.be/3yNoy4H2Z-o
  - Useful notes/diagrams on waves: http://hyperphysics.phy-astr.gsu.edu/hbase/Waves/watwav2.html, http://hyperphysics.phy-astr.gsu.edu/hbase/watwav.html#c1
  - Nice slides on natural wave phenomena http://www2.ess.ucla.edu/~schauble/EPSS15_Oceanography/LEC13S17_Waves_6perpage.pdf
  - Demonstration that Gerstner wave motion is physically possible https://www.tandfonline.com/doi/abs/10.2991/jnmp.2008.15.S2.7
-->

<!--TODO: Add and organise these
* Weta - Synthesizing waves from animated heightfields - 2012 - deals with optimizing a physical ocean surface to match an artist authored shape, numerical issues with tanh(), eliminating overlaps, computing a 3D velocity field: http://cs.au.dk/~bang/publications/NielsenSoderstromBridsonTOG2012.pdf
* Hitman Ocean Technology - they mix a few systems together (thanks for link @ajweeks) https://www.eidosmontreal.com/en/news/hitman-ocean-technology
* Kass - derive / justify wave equation: http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.89.1204&rep=rep1&type=pdf


### Wave Theory



### Wave Simulation

* Mode splitting - surface + volume sim combined: http://www.hilkocords.de/publications/mode_splitting.pdf
* Boat interaction: https://www.youtube.com/watch?v=YK_Za2MY2a0 , paper: http://www.hilkocords.de/publications/open_water.pdf
* Setting up boat interactioin in maya: https://www.youtube.com/watch?v=O-8ow82gQw8 . Touches on issues related to combining heightfield with displacement texture, and the wake lagging behind the object.
* Water Surface Wavelets - Jeschke et al. SIGGRAPH 2018 - http://visualcomputing.ist.ac.at/publications/2018/WSW/ - Interesting rederivation of water motion into a more computationally friendly form. The LOD system in Crest is very competitive with this technique.
* Lecture notes on numerical wave sim, makes use of Courant number directly - https://www.uio.no/studier/emner/matnat/ifi/nedlagte-emner/INF2340/v05/foiler/sim04.pdf
* Insomniac's Water Rendering System for Resistance 2: https://www.gamedevs.org/uploads/insomniac-water.pdf

### Wave Particles

* Original wave particles work: http://www.cemyuksel.com/research/waveparticles/
* Water Surface Wavelets: http://visualcomputing.ist.ac.at/publications/2018/WSW/

### 3D Simulation

* Bubble sim. Hill spherical vortex - irrotational flow around sphere. http://matthias-mueller-fischer.ch/publications/bubbles.pdf

-->
