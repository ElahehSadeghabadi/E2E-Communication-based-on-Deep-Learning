# End-to-End Deep Learning for Wireless Communication Systems
This repository contains a collection of detailed studies and implementations for designing end-to-end communication systems using deep neural networks. Leveraging the power of deep learning, this project explores how neural networks can act as both the transmitter (Tx) and receiver (Rx) to jointly optimize the physical layer of wireless links.

The material presented here progresses from foundational concepts to more complex scenarios, including various channel models and advanced MIMO techniques for both diversity and multiplexing gains. Each document provides theoretical background, system models, and code implementation details, making this an ideal resource for anyone interested in the practical application of deep learning in wireless communications.

# Project Structure and Contents
The repository is organized into five core PDF documents, each focusing on a specific aspect or channel model:

0. `Basics.ipynb`:  This foundational document lays out the essential concepts for end-to-end deep learning in communication systems.
   - **Key Topics:** Introduces the overarching system model where Tx and Rx are neural networks. Explores different signal representations (message indexing, one-hot encoding, binary encoding) and their impact on network design. Details important transmitter constraints (energy, amplitude, average power). Explains crucial evaluation metrics like Block Error Rate (BLER) and Bit Error Rate (BER), and methods for visualizing learned signal constellations (e.g., `t-SNE`).
   - **Purpose:** Serves as the theoretical groundwork and conceptual guide for understanding the subsequent implementations.

1. `1_AWGN.ipynb`:  
   This document provides the first practical example, implementing an end-to-end communication system over an Additive White Gaussian Noise (AWGN) channel.
   - **Key Topics:** Detailed setup of the communication autoencoder for a point-to-point, single-antenna system with an AWGN channel. Covers data generation, neural network architectures for the encoder and decoder, training methodology, and comprehensive performance evaluation using BLER and BER curves against $\frac{E_b​}{N_0}$​.
   - **Purpose:** Demonstrates the basic principles of deep learning applied to a fundamental communication channel.

2. `2_Interference_Channel.ipynb`:  
   Moving beyond single-user systems, this document explores an end-to-end deep learning approach for a two-user interference channel.
   - **Key Topics:** Models a scenario where two transmitters communicate with their respective receivers, experiencing mutual interference and AWGN. The implementation shows how neural networks can be designed to handle and potentially mitigate interference in a complex multi-user environment. Focuses on complex-valued signals and noise.
   - **Purpose:** Illustrates the application of deep learning to solve problems in multi-user communication and interference management.

3. `3_MIMO_for_Diversity.ipynb`:  
   This document delves into Multiple-Input Multiple-Output (MIMO) systems, specifically focusing on achieving spatial diversity.
   - **Key Topics:** Presents a point-to-point MIMO system with block fading, where deep learning is used to enhance communication reliability. It considers scenarios without Channel State Information at the Transmitter (CSIT) but with CSIR (Channel State Information at the Receiver), mimicking open-loop MIMO systems where Space-Time Block Codes (STBC) are traditionally used.
   - **Purpose:** Demonstrates how deep learning can design robust encoders and decoders to exploit spatial diversity in fading channels.

4. `4_MIMO_for_Multiplexing_Gain.ipynb`:  
   Continuing the exploration of MIMO, this document focuses on achieving spatial multiplexing gain using deep learning.
   - **Key Topics:** Explores a $2\times 2$ MIMO system with block fading, assuming perfect Channel State Information at both the Transmitter and Receiver (CSIT and CSIR). This allows for joint optimization of modulation and beamforming to transmit multiple independent data streams simultaneously, thereby increasing throughput.
   - **Purpose:** Illustrates how deep learning can maximize data rates by effectively utilizing spatial multiplexing in MIMO systems.

5. `5_Generative_Model_for_Channel.ipynb`:

6. `6_Broadcast_Channel.ipynb`:
   - **Key Topics:**
   - **Purpose:** 

# Getting Started
To explore the content of this repository, you can simply view the attached .ipynb Jupyter notebook files. Each notebook functions as a self-contained tutorial, including explanations, system models, and code outputs. For more details, refer to the corresponding papers cited below.

## Recommended Workflow:
- Begin with `Basics.ipynb` to grasp the fundamental concepts.
- Proceed to `1 AWGN.ipynb` for a foundational implementation.
- Then, explore the more advanced scenarios in `2_Interference_Channel.ipynb`, `3_MIMO_for_Diversity.ipynb`, `4_MIMO_for_Multiplexing_Gain.ipynb`, `5_Generative_Model_for_Channel.ipynb`, and `6_Broadcast_Channel.ipynb`.

# Future Enhancements

Stay tuned for updates as this repository evolves to provide a more interactive and accessible learning experience!

# Contributing
Contributions are highly encouraged! If you have suggestions for improvements, new examples, bug fixes, or wish to help with the conversion to Jupyter notebooks, please feel free to:

- Open an issue to discuss your ideas.

- Submit a pull request with your proposed changes.

# References
[1] T. O'Shea and J. Hoydis, "*An Introduction to Deep Learning for the Physical Layer,*" in IEEE Transactions on Cognitive Communications and Networking, vol. 3, no. 4, pp. 563-575, Dec. 2017.

[2] T. J. O'Shea, T. Erpek and T. C. Clancy, "*Physical layer deep learning of encodings for the MIMO fading channel,*" 2017 55th Annual Allerton Conference on Communication, Control, and Computing (Allerton), Monticello, IL, USA, 2017, pp. 76-80.

[3] H. Ye, G. Y. Li, B. -H. F. Juang and K. Sivanesan, "*Channel Agnostic End-to-End Learning Based Communication Systems with Conditional GAN,*" 2018 IEEE Globecom Workshops (GC Wkshps), Abu Dhabi, United Arab Emirates, 2018, pp. 1-5.

[4] J. Song, C. Häger, J. Schröder, T. J. O'Shea, E. Agrell and H. Wymeersch, "*Benchmarking and Interpreting End-to-End Learning of MIMO and Multi-User Communication*," in IEEE Transactions on Wireless Communications, vol. 21, no. 9, pp. 7287-7298, Sep. 2022.

# License
This project is licensed under the MIT License - see the `LICENSE` file for details.
