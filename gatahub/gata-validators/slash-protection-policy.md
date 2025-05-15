---
description: >-
  GATA HUB validators are slash-protected. Learn more about GATA HUB's slash
  protection policy.
---

# Slash Protection Policy

### Types of Slashing

There are two types of slashings validator nodes might face:

* **Downtime** (when the validator is unable to sign most of the blocks in the particular window)
* **Double signing** (double signing occurs when a validating entity / private key submits two signed messages for the same block)&#x20;

### **Coverage of Slashing**

* 100% downtime slashing coverage in a maximum of 14-28 days
* 10% double signing coverage in a maximum of 14-28 days \
  &#xNAN;_(we hope to increase this number in the future)_&#x20;

Because every network has different slashing parameters, we cannot give you estimates, but let's take Juno Network as an example: if you delegate 100 $JUNO to GATA HUB and the validator gets downtime slashed you would be slashed 0.01 JUNO and 5 $JUNO in case of a double sign slashing.

### **Slashing Refund-Time**

* 14-28 days depending on the network from where we are unbounding to cover the loss.&#x20;

### **Eligible Chains**

* **Cosmos Hub**
* **Atom One**
* **Juno**
* **Omniflix**
* **Akash Network**
* **Stargaze**

### **Past Slash/Refund Events**

#### **Passage validator**&#x20;

October 2023: unknown reasons, resulting in downtime slash.&#x20;

{% file src="../../../.gitbook/assets/gata_passage_delegator_slash_refund.xlsx" %}
PASG Slashing 2023-10
{% endfile %}

#### **Akash validator**

November 2023: node traffic got stuck and validator lost connection to peers, resulting in downtime slash.&#x20;

{% file src="../../../.gitbook/assets/gata_akash_delegator_slash_refund.xlsx" %}
AKT Slashing 2023-11
{% endfile %}

#### Cosmos HUB

February 11, 2024: validator lost connection to peers during infrastructure upgrade, resulting in downtime slash.&#x20;

{% file src="../../../.gitbook/assets/Slash amount Cosmos HUB 11Feb 2024.txt" %}
ATOM Slashing 2024-02
{% endfile %}

March 5, 2025: Validator slashed because of Stride ICS chain downtime.&#x20;



{% file src="../../../.gitbook/assets/GATA_Cosmos_D_Slash_refund.txt" %}
ATOM slashing 2025-03
{% endfile %}
