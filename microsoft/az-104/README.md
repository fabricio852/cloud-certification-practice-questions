# AZ-104 Practice Questions: Microsoft Certified: Azure Administrator Associate

[← All certifications](../../README.md)

5 free, original AZ-104 practice questions with an explanation for every option.

> **Want the full bank?** Practice [400+ AZ-104 questions and a 50-question timed mock exam on CLOUD.VERSE](https://cloudverse.pro/microsoft/az-104/practice-exam?utm_source=github&utm_medium=readme&utm_campaign=free-practice-questions&utm_content=az-104). You get 15 free questions per day.

## Exam at a glance

| | |
|---|---|
| Exam code | AZ-104 |
| Certification | Microsoft Certified: Azure Administrator Associate |
| Exam duration | 100 minutes |
| Passing score | 700 (scaled 100–1000) |
| CLOUD.VERSE mock exam | 50 questions in 100 minutes |
| Official exam guide | [Microsoft Learn](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-104) |

Exam details can change. Always confirm them in the official guide.

## Domains

| Domain | Weight |
|---|---|
| Manage Azure identities and governance | 20–25% |
| Implement and manage storage | 15–20% |
| Deploy and manage Azure compute resources | 20–25% |
| Implement and manage virtual networking | 15–20% |
| Monitor and maintain Azure resources | 10–15% |

## Questions

Answer each question before you open **Show answer**.

### Question 1 · Manage Azure identities and governance

Your company must ensure that resources in a subscription are created only in the West Europe and North Europe regions. What should you use?

- **A.** An Azure RBAC role assignment
- **B.** An Azure Policy assignment that uses the built-in Allowed locations policy
- **C.** A resource lock
- **D.** Tags on the subscription

<details>
<summary><b>Show answer</b></summary>

**Correct answer: B. An Azure Policy assignment that uses the built-in Allowed locations policy**

- ❌ **A. An Azure RBAC role assignment.** RBAC controls who can perform which actions. It cannot restrict where resources are deployed.
- ✅ **B. An Azure Policy assignment that uses the built-in Allowed locations policy.** Azure Policy evaluates resource properties when resources are created or updated, and it denies deployments outside the allowed regions.
- ❌ **C. A resource lock.** Locks prevent deletion or modification of existing resources. They do not control location.
- ❌ **D. Tags on the subscription.** Tags are metadata for organization and cost reporting. They enforce nothing.

</details>

### Question 2 · Manage Azure identities and governance

A production resource group must be protected from accidental deletion. Administrators still need to update the resources inside it. What should you apply?

- **A.** A ReadOnly lock on the resource group
- **B.** Assign the Reader role to all administrators
- **C.** A CanNotDelete (Delete) lock on the resource group
- **D.** Move the resource group to a new subscription

<details>
<summary><b>Show answer</b></summary>

**Correct answer: C. A CanNotDelete (Delete) lock on the resource group**

- ❌ **A. A ReadOnly lock on the resource group.** A ReadOnly lock also blocks updates, which administrators still need.
- ❌ **B. Assign the Reader role to all administrators.** Reader removes the ability to modify resources.
- ✅ **C. A CanNotDelete (Delete) lock on the resource group.** A Delete lock allows reads and updates but blocks deletion. Resources in the group inherit it.
- ❌ **D. Move the resource group to a new subscription.** Moving resources does not protect them from deletion.

</details>

### Question 3 · Implement and manage storage

A storage account holds data that must stay readable even if the primary region has an outage, without waiting for a failover. Which redundancy option should you choose?

- **A.** Locally redundant storage (LRS)
- **B.** Zone-redundant storage (ZRS)
- **C.** Geo-redundant storage (GRS)
- **D.** Read-access geo-redundant storage (RA-GRS)

<details>
<summary><b>Show answer</b></summary>

**Correct answer: D. Read-access geo-redundant storage (RA-GRS)**

- ❌ **A. Locally redundant storage (LRS).** LRS keeps three copies in a single datacenter. A regional outage makes the data unavailable.
- ❌ **B. Zone-redundant storage (ZRS).** ZRS spreads copies across availability zones in one region. It does not protect against a regional outage.
- ❌ **C. Geo-redundant storage (GRS).** GRS replicates to a secondary region, but you can read from it only after a failover.
- ✅ **D. Read-access geo-redundant storage (RA-GRS).** RA-GRS replicates data to a secondary region and lets you read from the secondary endpoint at any time.

</details>

### Question 4 · Deploy and manage Azure compute resources

You deploy two virtual machines that run the same web application. The VMs must keep running if an entire datacenter in the Azure region fails. What should you do?

- **A.** Deploy the VMs to different availability zones
- **B.** Place both VMs in the same availability set
- **C.** Use Premium SSD managed disks
- **D.** Place both VMs in a proximity placement group

<details>
<summary><b>Show answer</b></summary>

**Correct answer: A. Deploy the VMs to different availability zones**

- ✅ **A. Deploy the VMs to different availability zones.** Availability zones are physically separate datacenters within a region, with independent power, cooling, and networking.
- ❌ **B. Place both VMs in the same availability set.** An availability set spreads VMs across fault and update domains inside one datacenter. It protects against rack failures, not the loss of a datacenter.
- ❌ **C. Use Premium SSD managed disks.** Premium SSDs improve disk performance. They do not add redundancy across datacenters.
- ❌ **D. Place both VMs in a proximity placement group.** A proximity placement group keeps VMs physically close for low latency, which is the opposite of the requirement.

</details>

### Question 5 · Implement and manage virtual networking

Two virtual networks in the same region host services that must communicate privately with low latency. You want the simplest option, with no gateways to manage. What should you configure?

- **A.** A VNet-to-VNet VPN connection through VPN gateways
- **B.** Virtual network peering
- **C.** Service endpoints
- **D.** Azure Front Door

<details>
<summary><b>Show answer</b></summary>

**Correct answer: B. Virtual network peering**

- ❌ **A. A VNet-to-VNet VPN connection through VPN gateways.** This works, but it requires gateways to deploy and pay for, and it adds latency. It is not the simplest option.
- ✅ **B. Virtual network peering.** Peering connects the VNets over the Microsoft backbone using private IP addresses, with no gateway required.
- ❌ **C. Service endpoints.** Service endpoints secure traffic from a subnet to Azure PaaS services. They do not connect two VNets.
- ❌ **D. Azure Front Door.** Front Door is a global entry point for public web applications, not private VNet-to-VNet connectivity.

</details>

## Keep practicing

Five questions cover only a small part of the AZ-104 exam guide. On CLOUD.VERSE you get:

- 400+ AZ-104 practice questions with explanations
- A 50-question timed mock exam (100 minutes)
- 15 free questions per day

**[Practice AZ-104 on CLOUD.VERSE →](https://cloudverse.pro/microsoft/az-104/practice-exam?utm_source=github&utm_medium=readme&utm_campaign=free-practice-questions&utm_content=az-104)**

---

<sub>Independent project, not affiliated with or endorsed by Microsoft. These are original practice questions, not real exam questions, and they do not guarantee a passing score.</sub>
