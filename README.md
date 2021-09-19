# EC601-Project-1-Photonic-Circuits-for-ML
a literature review of photonic circuits for machine learning

Topic
Photonic chips are integrated circuits that use light (photon particles) to store, process and communicate information. They offer an alternative to electronic ICs while providing projected benefits of ~1000 times faster computation than electronic chips while also greatly reducing heat and energy consumption. 
Why is it important
To achieve better computing power with electronics, the size of transistors must go down to fit more on an IC. Reducing their size is becoming increasingly difficult and time consuming while also introducing new problems with each step. As of 2021 there are fabs capable of producing 2nm length transistors (about the wavelength of an ultraviolet ray). As transistors get smaller, inherent resistances increase which increases switching delay and power consumption, quantum mechanics becomes more impactful, and in general we see many diminishing returns from transistor size reduction. Silicon photonics provides a reasonably cost-effective way to fabricate photonic circuits to circumvent these issues. Photonics could also provide avenues to develop faster classical computers as well as accessible and scalable quantum computers.


Applications and societal Importance
While raw data in the world is increasing at astronomic rates our capability to process it all is waning. Deep learning requires 1000+ neural net layers and the global time and energy consumption to create convolutional filters and optimize cost functions between layers staggeringly large and ever increasing. Using photonic integrated circuits to store and process data could potentially lower that energy cost by over 3 orders of magnitude.

Literature review
While Silicon as a material is not optimal for creating photonic circuits, it is the material with which most chip fabs have the capability to create integrated circuits with. Silicon photonics still provides many benefits over electronics and will serve as a good transitionary material until new fabs and research will allow us to work with better suited materials [5]. 

There are multiple proposed methods to building photonic chips such as 3D printing whole chips with diffractive elements to create light interference for the processing of optical data or using nanophotonics to create beam splitters and directional couplers which can be difficult to scale to very deep layered networks. The method this paper proposes uses homodyne detectors to perform computation through light interference and allows for deep network scaling. The main power consumption occurs where optical signals are converted to or from electrical signals at the input and output of each layer. Photonic chips are a method for getting around the Landauer limit for computational energy. The Landauer principle states that for irreversible computing there is a minimum limit for energy loss in a system where some amount of information is deleted. In layman’s terms, if information is stored as energy and is deleted then the energy stored for that information is lost to the system and must be reintroduced from a power source. The Landauer physical limit for a typical MAC (multiply and accumulate) is 3 attojoules. However, in the case of photonic chips, the multiply step can completed via interference and is reversible (can be returned to a previous state). Thus, the computational energy of multiplication is kept in the system and allows for sub-Landauer energy limits per MAC [5]. 

Quantum computing also shows a lot of promise in the realm of machine learning. The basic concept is that applying a non-deterministic algorithm to minimize cost functions through many layers of backpropagation could greatly improve the speed of training computation. Essentially any problem that can be represented as a graph problem (in NP) can be solved by a quantum (non-deterministic) computer [1,2,4].

The use of photonics in quantum computing also provides benefits of unperturbed data communication between qumodes (a more general qubit) while working at room temperature and allows for small integrated circuit design. In both classical and quantum photonic circuits electronics are still employed in tandem, but their use is drastically reduced [1,2,7].

Open-Source Tools
•	Penny Lane: https://pennylane.ai/ 
•	Strawberry Fields: https://strawberryfields.ai/ 
Penny Lane and Strawberry Fields are both python libraries meant for simulating quantum circuits and algorithms that will interact with emulations of quantum computers on classical computers as well as actual quantum computers if you happen to have access to one. Strawberry Fields is for general programming of a photonic quantum hardware like the developer Xanadu’s quantum photonic computer and Penny Lane is a library built from Strawberry Fields for quantum machine learning.
Both Penny Lane and Strawberry fields have example code and tutorials to follow along with but it’s best to find some good footing in quantum mechanics before going forward into these because the syntax is meant to describe a photonic circuit that operates according to the physical principles of quantum mechanics. 
•	https://github.com/BYUCamachoLab/simphony 
Another open-source library for photonic circuit design is Simphony. A python tool from BYU with several standard photonic circuit elements to model the physical behavior of photonic circuits that are connected as components to build larger components. You can define physical parameters of circuit elements like waveguide thickness for instance.
Quantum photonic hardware
1.	https://www.youtube.com/watch?v=GSGM8iV8ZRU 
2.	https://arxiv.org/pdf/2103.02109.pdf 
Quantum Error Correction
3.	https://arxiv.org/pdf/2104.03241.pdf 
Quantum Machine Learning
4.	https://pennylane.ai/qml/whatisqml.html 
Deep Neural Networks and Hardware
5.	https://www.rle.mit.edu/eems/wp-content/uploads/2017/11/2017_pieee_dnn.pdf
Classical Photonic Computing
6.	https://journals.aps.org/prx/pdf/10.1103/PhysRevX.9.021032 
7.	https://www.youtube.com/watch?v=CBhdLTTbYoM 
