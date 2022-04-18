## EC2 - Pricing Model

### **[EC2 has 4 pricing models](https://aws.amazon.com/ec2/pricing/)**

1. On-Demand
2. Spot
3. Reserved Instances (RI)
4. Dedicated 



### **[On-Demand](https://aws.amazon.com/ec2/pricing/on-demand/)** (Least Commitment)

* Pay-As-You-Go (PAYG) model, where you consume compute and then you pay
* Default EC2 instince pricing
* No up-front payment and no long-term commitment
* Charged by the hour or by the minute (varies based on EC2 Instance Types)
* Low cost and flexible
* Short-term, spiky, unpredictable workloads

### **[Reserved Instances](https://aws.amazon.com/ec2/pricing/reserved-instances/)** up to 75% off (Best Long-term)

* Designed for applications that have a steady-state, predictable usage, or require reserved capacity
* Steady-state or predictable usage
* Commit to EC2 over a 1 or 3 year
* Can resell unused reserved instances 

* **Class Offerings** - The less flexible the greater the savings

    * **Standard**: Up to 75% reduced pricing compared to on-demand. You can modify RI Attributes.

    * **Convertible**: Up to 54% reduced pricing compared to on-demand. You can exchange RI based on RI Attributes if greater or equal in value.

    * **Scheduled**: AWS no longer offers Scheduled RI

* **Payment Options** - The greater upfront the great the savings

    * All Upfront

        * Full payment is made at the start of the term

    * Partial Upfront

        * A portion of the cost must be paid upfront and the remaining hours in the term are billed at a discounted hourly rate

    * No Upfront

        * You are billed a discounted hourly rate for every hour within the term, regardless of whether the Reserved Instance is being used

        * RIs can be shared between multiple accounts within an organization

        * Unused RIs can be sold in the Reserved Instance Marketplace.


### **[Spot Pricing](https://aws.amazon.com/ec2/spot/)** up to 90% (Biggest Savings)

* AWS has unused compute capacity that they want to maximize the utility of their idle servers. It’s like when a hotel offers booking discounts to fill vacant suites or planes offer discounts to fill vacant seats
* Request spare computing capacity
* Flexible start and end times
* Can handle interruptions (server randomly stopping and starting)
* For non-critical background jobs 

### **[Dedicated Hosting](https://aws.amazon.com/ec2/dedicated-hosts/)** (Most Expensive)

* When you have strict server-bound licensing that won’t support multi-tenancy or cloud deployments you use Dedicated Hosts.
* Can be on-demand or reserved (up to 75% off)
* When you need a guarantee of isolate hardware (enterprise requirements)
* Dedicated can be offered for:

    * On-demand
    * Reserved (up to 60% savings)
    * Spot (up to 90% savings) 

