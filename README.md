# keyaggprotocol
Robust Authentication Protocol for WMSN using Blockchain and PUF
Introduction
In the era of the Internet of Medical Things (IoMT), patients and doctors can access various healthcare services via wireless communication technology without visiting the hospital in person. However, the transmission of sensitive information over insecure channels exposes these systems to various security threats. To address these challenges, robust and lightweight authentication protocols are essential for ensuring dependable healthcare services in Wireless Medical Sensor Networks (WMSN).

Problem Statement
Wang et al. proposed a blockchain and physically unclonable functions (PUFs)-based lightweight authentication protocol for WMSN, claiming it to be resistant to various cyber and physical security threats while meeting necessary security requirements. However, our analysis shows that Wang et al.’s protocol is vulnerable to multiple security attacks, such as man-in-the-middle and session key disclosure attacks, and lacks mutual authentication.

Our Solution
To address these issues, we propose a robust authentication protocol for WMSN using blockchain and PUF. Our scheme enhances security by addressing the identified vulnerabilities in Wang et al.'s protocol. The proposed protocol ensures mutual authentication and is resistant to a wide range of security attacks.

Methodology
We assess the security of the proposed protocol through both informal and formal security analyses, including:

AVISPA Simulation: A powerful tool for automated validation of internet security protocols.
ROR Oracle Model: A model used to analyze the resistance of cryptographic protocols against replay and other attacks.
Scyther Tool: For formal verification of security protocols, ensuring the protocol's resilience against attacks such as man-in-the-middle, session key disclosure, and others.
Implementation Details
Protocol Roles
The protocol includes three main roles: Data Authority (DA), Data Buyer (DB), and Certificate Authority (CA). The communication flow and security claims are described as follows:

Data Authority (DA)

Initiates the authentication process by sending a certificate to DB.
Exchanges nonces and public keys with DB to establish a session key.
Claims secrecy of the session key and other sensitive information.
Data Buyer (DB)

Receives a certificate from DA and forwards it to CA for validation.
Exchanges nonces and public keys with DA to establish a session key.
Sends the established session key to CA for confirmation.
Claims secrecy of the session key and other sensitive information.
Certificate Authority (CA)

Validates the certificate received from DB.
Confirms the successful establishment of a secure session.
Security Claims
Each role in the protocol claims various security properties such as:

Secret: Ensures the confidentiality of exchanged messages and session keys.
Alive: Confirms the involvement and active participation of each entity.
Weakagree, Niagree, Nisynch: Guarantees the agreement and synchronization between the communicating entities.
How to Use
Prerequisites
To run the simulation, ensure that you have the following tools installed:

Scyther: A tool for automatic verification of security protocols.
Installation
Clone the repository:
bash
Copy code
git clone <repository-url>
Navigate to the project directory:
bash
Copy code
cd <project-directory>
Running the Simulation
Open the Scyther tool.
Load the protocol definition file (protocol.spdl).
Run the simulation to analyze the security properties.
Check the results for any potential vulnerabilities or confirmation of security claims.
Results Interpretation
The output will indicate whether the protocol is secure against various types of attacks. Ensure to review the detailed analysis provided by the tool.
Contributions
We welcome contributions from the community. If you have suggestions or improvements, please fork the repository and submit a pull request.

License
This project is licensed under the MIT License. See the LICENSE file for details.

References
Wang et al., "Blockchain and PUF-Based Lightweight Authentication Protocol for WMSN," IEEE Internet of Things Journal, DOI: 10.1109/JIOT.2021.3117762.
For more detailed information, please refer to the full paper.
