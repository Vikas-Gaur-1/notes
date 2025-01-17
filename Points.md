# Quantum Mechanics Foundations of Quantum Key Distribution (QKD)

## 1. Heisenberg's Uncertainty Principle
### Core Concept
- Fundamental quantum mechanics principle stating that certain pairs of physical properties cannot be simultaneously measured with absolute precision
- In a quantum system, only one property of conjugate properties (like position and momentum) can be known with certainty

### Implications for QKD
- Measurement inherently disturbs the quantum system
- Photon polarization used as a key mechanism for secure communication
- Any unauthorized measurement will introduce detectable changes in the quantum state

## 2. No Cloning Theorem
### Core Concept
- It is fundamentally impossible to create perfect, identical copies of an unknown quantum state
- Prevents unauthorized duplication of quantum information

### Security Implications
- Provides a natural mechanism for detecting eavesdropping
- Any attempt to intercept or copy quantum information will introduce detectable anomalies
- Ensures the integrity of quantum communication channels

## 3. Quantum Entanglement
### Core Concept
- Quantum particles can become entangled, sharing correlated states regardless of physical distance
- Measurement of one particle instantaneously affects its entangled partner

### Applications in Quantum Communication
- Basis for advanced quantum communication protocols
- Enables quantum teleportation through classical information channels
- Fundamental to protocols like Eckert's protocol for secure key distribution

-------------------------------------------------------------------------------------------------------------

# QKDNetSim Component Diagram

![sim-components](https://github.com/user-attachments/assets/bec80e09-d38c-426a-b61d-e078129f7c65)

It has two major modules in the QKDNetSim system: **QKD Core** (left) and **QKD Application** (right).

---

## **QKD Core**

The **QKD Core** module includes fundamental components responsible for generating, managing, and processing quantum keys. These are the building blocks for secure communication. The components are:

1. **QKD Key**
   - Represents the quantum key object with attributes like key size, key value, and state.

2. **QKD Buffer**
   - Stores the generated quantum keys and manages thresholds for key availability.

3. **QKD Control**
   - Manages and monitors the QKD system's operations.

4. **QKD Encryptor**
   - Responsible for encryption processes using QKD keys.

5. **QKD Helpers**
   - Provides additional functionalities for the QKD system.
   - Subcomponents:
     - **QKD App Helper**: Assists applications in utilizing QKD keys.
     - **QKD Link Helper**: Facilitates link-level operations and key exchanges.

---

## **QKD Application**

The **QKD Application** module includes components that implement application-level functionality and post-processing mechanisms for QKD-based systems. The components are:

1. **QKD Post-Processing**
   - Handles key establishment and supplies keys to the Key Management System (KMS).

2. **QKD Key Manager System**
   - Manages the distribution and lifecycle of QKD keys for applications.

3. **QKD Cryptographic Applications**
   - Represents cryptographic applications that utilize QKD keys for secure communication.

4. **QKD Application 004**
   - A specific application designed for implementing QKD standards.

5. **QKD Application 014**
   - Implements the ETSI QKD 014 client and manages the fetching and utilization of keys.

---

### **Overview of the Interaction**

- The **QKD Core** module provides essential services such as key generation, storage, and encryption. It forms the backbone of the system.
- The **QKD Application** module uses these services to perform application-specific tasks like secure communication, post-processing, and cryptographic operations.

This modular design ensures scalability and reusability across different quantum key distribution scenarios.


-------------------------------------------------------------------------------------------------------------
# QKDNetSim UML Diagram  

![qkd_model_uml](https://github.com/user-attachments/assets/c55edd68-16f8-4def-bcdb-744d03470a0f)


## QKD Post-Processing  

### Core Concept  
- Represents the process of key establishment in a QKD system.  
- Generates and supplies keys to the Key Management System (KMS) at regular intervals.  

### Essential Parameters  
- **`key size`**: Size of the generated keys  
- **`key rate`**: Rate at which keys are generated  
- **`packet size`**: Size of the packets used to transmit the keys  
- **`data rate`**: Rate at which data is transmitted  
- **`network traffic intensity`**: Intensity of the network traffic  

---

## QKD Key  

### Core Concept  
- Represents the ITS (Information-Theoretically Secure) crypto key generated by the QKD system  

### Essential Parameters  
- **`id`**: Unique key identifier  
- **`key size`**: Size of the key  
- **`key value`**: Actual value of the key  
- **`key state`**: Current state of the key  
- **`timestamp`**: Timestamp associated with the key  
- **`module identifier`**: Identifier of the module that generated the key  

---

## QKD Buffer  

### Core Concept  
- Stores newly generated QKD keys for secure access  

### Essential Parameters  
- **`minKeyBit`**: Lower threshold value for the number of keys in the buffer  
- **`thrKeyBit`**: Threshold value for the number of keys in the buffer  
- **`maxKeyBit`**: Upper threshold value for the number of keys in the buffer  
- **`defaultKeySize`**: Default size of the stored keys  
- **`status`**: Current state of the buffer  

---

## QKD Key Management System (KMS)  

### Core Concept  
- Collects, manages, distributes, and supplies QKD keys for secure communication  

### Essential Parameters  
- **`id`**: KMS identifier  
- **`maxKeyPerRequest`**: Maximum number of keys supplied in a single request  
- **`minKeySize`**: Minimum allowed key size  
- **`maxKeySize`**: Maximum allowed key size  
- **`KMSidentifier`**: Unique identifier of the KMS  

---

## QKD Crypto Applications  

### Core Concept  
- Applications consuming QKD keys for cryptographic purposes  

### Essential Parameters  
- **`id`**: Application identifier  
- **`remoteId`**: Remote application identifier  
- **`packetSize`**: Size of the packets used for the application  
- **`dataRate`**: Data rate of the application  
- **`encryption`**: Encryption algorithm used  
- **`authentication`**: Authentication algorithm used  
- **`keyLifetime`**: Lifetime of the keys  
- **`authTagSize`**: Size of the authentication tag  

---

## QKD Application 014  

### Core Concept  
- Specific application implementing the ETSI QKD 014 client  

### Essential Parameter  
- **`numberOfKeys`**: Number of keys to fetch in a single request  

---

The diagram illustrates the relationships between these components and their interactions, highlighting the flow of key generation, management, storage, and consumption within the QKD system. The essential parameters ensure proper configuration and functioning of the QKD system.  
