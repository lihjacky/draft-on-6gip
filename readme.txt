=== English Summary of: draft-li-6gip-fine-grained-privacy-network-00 ===
Title: Future Requirements of Fine-Grained Privacy for the Network
Authors: Lun Li (Huawei), Faye Liu (Huawei Singapore)
Date: July 4, 2025
Category: Informational (IETF Internet-Draft)

--- Overview ---

This Internet-Draft, submitted to the IETF 6GIP (6G IP) group, explores new privacy
requirements for future networks (beyond 5G, towards 6G and IMT-2030). It argues that
existing network privacy protections mainly focus on data transmission and identity
concealment (e.g., SUPI/GUTI in 5G), but largely overlook the data processing and
management phases—where privacy vulnerabilities are emerging due to the growing use
of computing power for data analytics and sensing services.

--- Key Motivation ---

1. ITU-R IMT-2030 framework envisions future networks processing data rather than
   merely transmitting it. This introduces new privacy risks in the data processing
   stage of the data lifecycle.
2. New regulations (EU Data Act, eIDAS 2.0) demand stronger data sovereignty and
   lifecycle-wide privacy protection.
3. Individual users want fine-grained control: they may relax or escalate privacy
   levels depending on context (home vs. public, type of service), choose where data
   is processed (operator-side vs. third-party), and specify which privacy-enhancing
   techniques are applied.

--- Use Cases and Privacy-as-a-Service (PrivaaS) ---

The draft introduces a "Privacy as a Service" (PrivaaS) concept with three
illustrative users:

  - User A (web browsing): Anonymization of identity identifiers to prevent traffic
    correlation by attackers.
  - User B (data sharing with third party): Data pseudonymization and location
    scoping (e.g., approximate location instead of precise coordinates).
  - User C (autonomous driving): Homomorphic encryption for environment sensing
    data, enabling computation on encrypted data for obstacle detection.

Each user gets a fine-grained privacy mechanism tailored to their service type,
subscription/context, and network state.

--- Proposed Privacy-Enhancing Technologies ---

The draft lists several candidate technologies for processing-phase privacy:

  1. Ciphertext Computation (Homomorphic Encryption) — compute directly on
     encrypted data without decryption.
  2. Private Information Retrieval (PIR) — query a server without revealing which
     item is being queried (Apple's PIR at WWDC25 cited as industry reference).
  3. Private Set Intersection (PSI) — compare the intersection of private datasets
     across parties without leaking individual data (useful in federated learning).
  4. Multi-Party Computation (MPC) — distributed participants jointly compute a
     function over private inputs while keeping each input secret.

--- Related IETF/IRTF Groups ---

The draft identifies potential relevant working groups:

  - 6GIP: directly focused on 6G network privacy and security.
  - PPM (Privacy Preserving Measurement): MPC-based protocols for measurement.
  - PEARG (Privacy Enhancements and Assessments Research Group): general forum for
    privacy-enhancing technologies in network protocols.
  - CFRG (Crypto Forum Research Group): cryptographic mechanisms and latest
    algorithmic advances.

--- Current Status ---

The draft is in early stage. Several sections (AI/ML use case, security
considerations, acknowledgments) are marked as #TODO. It aims to attract IETF/IRTF
interest for protocol-level research on fine-grained privacy for future networks.

--- References ---

- RFC 2119 (Key words for requirement levels)
- ITU-R IMT-2030 Framework (ITU, May 2024)
- 3GPP TS 22.261 (5G service requirements)
- EU Data Act and eIDAS 2.0 (European digital identity regulation)
