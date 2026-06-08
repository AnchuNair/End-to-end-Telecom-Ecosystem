# Telecom Ecosystem: Network, OSS, BSS, Policy & Charging

## Overview

Modern telecommunications is much more than mobile towers and internet connectivity.

A telecom operator is a complex ecosystem where network infrastructure, business systems, customer management, charging systems, automation platforms, and cloud-native technologies work together to deliver services to millions of subscribers.

This repository serves as a knowledge base for understanding the complete telecom landscape, including:

- Access Network (RAN)
- Transport Network
- Core Network
- OSS
- BSS
- Policy Control
- Charging Systems
- Service Provisioning
- Service Assurance
- Cloud-Native Telecom
- AI and Automation

---

# Telecom Architecture at a Glance

                     Subscriber
                          |
                          |
                    +-----------+
                    |    RAN    |
                    | (gNodeB)  |
                    +-----------+
                          |
                          |
                  +---------------+
                  |  Transport    |
                  |  Network      |
                  +---------------+
                          |
                          |
                  +---------------+
                  |  Core Network |
                  +---------------+
                          |
          ----------------------------------
          |                |               |
          |                |               |
         PCF             CHF             UDM
          |                |
          |                |
     -----------------------------
     |                           |
     |        OSS/BSS            |
     |                           |
     -----------------------------

---

# Part 1: Network Domain

The Network Domain is governed primarily by 3GPP specifications.

Its responsibility is to provide connectivity and transport data traffic securely and efficiently.

## Network Layers

### 1. Access Network (RAN)

The Radio Access Network connects mobile devices to the telecom network.

#### Evolution

| Generation | Component |
|------------|------------|
| 2G | BTS |
| 3G | NodeB |
| 4G | eNodeB |
| 5G | gNodeB |

#### Responsibilities

- Radio communication
- Mobility management
- Handover execution
- Radio scheduling
- Signal transmission

#### Key Concepts

- Cell
- Sector
- Carrier Aggregation
- Massive MIMO
- Beamforming

---

### 2. Transport Network

The transport network carries traffic between RAN and Core.

#### Components

- Fiber Optics
- Ethernet Switches
- IP Routers
- MPLS Routers
- Microwave Links

#### Responsibilities

- Packet forwarding
- Traffic engineering
- Network resilience
- Low latency transport

---

### 3. Core Network

The core network acts as the control and service layer.

---

## 4G EPC Components

### MME

Mobility Management Entity

Responsibilities:

- Subscriber registration
- Mobility management
- Authentication coordination

### SGW

Serving Gateway

Responsibilities:

- User plane anchoring
- Packet forwarding

### PGW

Packet Gateway

Responsibilities:

- Internet connectivity
- PCC enforcement
- Charging integration

### HSS

Home Subscriber Server

Responsibilities:

- Subscriber profile management

### PCRF

Policy and Charging Rules Function

Responsibilities:

- Policy decision making
- QoS rule creation
- Charging control

---

## 5G Core Components

### AMF

Access and Mobility Management Function

Responsibilities:

- Registration
- Mobility management

### SMF

Session Management Function

Responsibilities:

- Session creation
- UPF selection

### UPF

User Plane Function

Responsibilities:

- Packet forwarding
- Traffic routing

### UDM

Unified Data Management

Responsibilities:

- Subscriber data storage

### AUSF

Authentication Server Function

Responsibilities:

- Authentication

### PCF

Policy Control Function

Responsibilities:

- Policy management
- QoS decisions

### CHF

Charging Function

Responsibilities:

- Online charging
- Offline charging

### NRF

Network Repository Function

Responsibilities:

- Service discovery

### NSSF

Network Slice Selection Function

Responsibilities:

- Slice assignment

---

# Part 2: Business Domain

The Business Domain manages customers, products, services, and revenue.

Primary frameworks:

- TM Forum eTOM
- ITIL
- SID Model

---

# OSS (Operations Support Systems)

OSS focuses on network and service operations.

## Functions

### Service Provisioning

Examples:

- SIM activation
- Broadband activation
- Service modification

### Fault Management

Examples:

- Alarm processing
- Root cause analysis

### Performance Management

Examples:

- KPI monitoring
- Network optimization

### Inventory Management

Examples:

- Device inventory
- Resource inventory

### Service Assurance

Examples:

- SLA monitoring
- Customer experience monitoring

### Orchestration

Examples:

- Automated workflows
- Zero-touch provisioning

---

# BSS (Business Support Systems)

BSS manages customer-facing business operations.

## Components

### CRM

Customer Relationship Management

Functions:

- Customer onboarding
- Customer support
- Customer profile management

### Product Catalog

Functions:

- Product definitions
- Offer management

### Order Management

Functions:

- Order capture
- Order fulfillment

### Billing

Functions:

- Invoice generation
- Payment processing

### Revenue Management

Functions:

- Revenue tracking
- Revenue assurance

---

# Policy and Charging Control (PCC)

PCC enables policy enforcement and charging decisions.

---

## PCC in 4G

Components:

- PCRF
- PCEF
- OCS

Flow:

Subscriber → PGW → PCRF → OCS

---

## PCC in 5G

Components:

- PCF
- CHF
- SMF
- UPF

Flow:

Subscriber → UPF → SMF → PCF → CHF

---

# Charging Systems

Charging systems bridge Network and Business domains.

---

## Online Charging System (OCS)

Used primarily for prepaid subscribers.

Functions:

- Balance management
- Real-time quota control
- Service authorization

---

## Offline Charging System (OFCS)

Used primarily for postpaid subscribers.

Functions:

- CDR collection
- Billing integration

---

## Charging Function (CHF)

5G evolution of charging systems.

Supports:

- Converged charging
- Service-based architecture
- HTTP/2 interfaces

---

# Service Lifecycle

## Step 1: Product Creation

BSS Product Catalog

↓

## Step 2: Customer Purchase

CRM / Order Management

↓

## Step 3: Service Provisioning

OSS Activation Systems

↓

## Step 4: Network Configuration

Core / RAN

↓

## Step 5: Usage

Voice / SMS / Data

↓

## Step 6: Charging

OCS / CHF

↓

## Step 7: Billing

Billing Systems

---

# Telecom Standards

## 3GPP

Defines:

- Mobile architecture
- Signaling protocols
- Security
- Core network

Examples:

- LTE
- 5G

---

## TM Forum

Defines:

- eTOM
- SID
- Open APIs

Focus:

- OSS
- BSS

---

## ITIL

Defines:

- Incident Management
- Change Management
- Problem Management

---

# Cloud-Native Telecom

Modern telecom functions run as cloud-native applications.

Technologies:

- Kubernetes
- Docker
- Helm
- OpenShift

Benefits:

- Scalability
- Resilience
- Automation

---

# Automation Platforms

Common technologies:

## Apache Kafka

Used for:

- Event streaming
- Real-time data integration

## Apache NiFi

Used for:

- Data ingestion
- Flow management

## Camunda

Used for:

- Workflow orchestration
- Business process automation

---

# AI and AIOps

Applications:

- Fault prediction
- Churn prediction
- Capacity forecasting
- Root cause analysis
- Network optimization

---

# Key Learning Roadmap

1. Telecom Fundamentals
2. LTE Architecture
3. 5G Core Architecture
4. OSS/BSS
5. PCC and Charging
6. Kafka
7. Camunda
8. Cloud-Native Telecom
9. AI in Telecom
10. End-to-End Service Assurance

---

# References

- 3GPP Specifications
- TM Forum eTOM
- TM Forum Open APIs
- ITIL Framework
- GSMA Technical Documents

---

Anchu

Telecom Knowledge Repository

Covering telecom architecture from RAN to OSS/BSS, policy control, charging systems, cloud-native platforms, and AI-driven operations.
