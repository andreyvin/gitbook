## Restoring Amazon Glacier Data

When choosing to restore data from [Amazon Glacier](https://aws.amazon.com/glacier/), you can select among the following three data retrieval modes:

* ### **Standard**

  This option is selected by default. It enables you to retrieve your data on time and on budget:

  * typical data retrieval time \(**3 **to **5 **hours\);

  * a cost of $**0.01**per GB, along with an extra charge of $**0.05 **for every **1,000 **requests.

* ### **Bulk**

  This is the best option for scheduled or non-urgent data retrieval. It features the lowest data retrieval speed at the lowest cost:

  * extended data retrieval time \(**5 **to **12 **hours\);

  * a cost of $**0.0025 **per GB

    ...and every **1000 **requests amounting to $**0.025**.

    **\[???\]**

* ### **Expedited**

  This mode features the highest data retrieval speed at the highest price:

  * the shortest possible data retrieval time \(**1 **to **5 **minutes\);

  * a cost of $**0.03 **per GB and $**0.01 **per request.

    **\[??? Explain and do we need to elaborate as follows:\]**

* **On-Demand**

  On-Demand requests are similar to EC2 On-Demand instances and are available most of the time.

* **Provisioned**

  Provisioned capacity guarantees that your retrieval capacity for expedited retrievals is available when you need it. Provisioned capacity units allow you to pay a fixed up-front fee to expedite retrievals from Amazon Glacier vaults for a given month.

  A unit of Provisioned capacity costs $**100 **per month and ensures that at least three expedited retrievals can be performed every five minutes and provides up to **150 **MB/s of retrieval throughput.

  **\[??? - If you exceed that limit, expect errors on the part of Amazon.\]**

You don't need to specify whether an expedited retrieval is On-Demand or Provisioned. If you have purchased provisioned capacity, then all expedited retrievals are automatically served through your provisioned capacity.

See the following document to learn more about this feature: [Provisioned Capacity](https://docs.aws.amazon.com/amazonglacier/latest/dev/downloading-an-archive-two-steps.html#api-downloading-an-archive-two-steps-retrieval-expedited-capacity).

