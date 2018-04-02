# Step 4 \(Optional\) - Restore Amazon Glacier Data

When using an Amazon cloud storage, you can choose whether to restore any files located in [Amazon Glacier](https://aws.amazon.com/glacier/) using the corresponding option on this wizard page.

![](https://github.com/robertzakiev/gitbook/tree/703d9f96af3546d5a85e17cd24df8e3834d130e4/assets/restore-glacier-data.png)

> In most cases, these files do not need to be restored and we recommend that you leave this option disabled. Otherwise, please be informed that restoring these files can be either too slow \(up to several hours\), or too expensive.
>
> However, if you still need to restore Amazon Glacier data, you can select the preferred data retrieval mode on the next wizard page by choosing the corresponding option.

When choosing to restore data from Amazon Glacier, you can select among the following three data retrieval modes:

* **Standard**

  This option is selected by default. It enables you to retrieve your data on time and on budget:

  * typical data retrieval time \(**3 **to **5 **hours\);
  * a cost of $**0.01 **per GB, along with an extra charge of $**0.05 **for every **1,000 **requests.

* **Bulk**

  This is the best option for scheduled or non-urgent data retrieval. It features the lowest data retrieval speed at the lowest cost:

  * extended data retrieval time \(**5 **to **12 **hours\);
  * a cost of $**0.0025 **per GB \(with every **1000 **requests amounting to $**0.025\)**.

* **Expedited**

  This mode features the highest data retrieval speed at the highest price:

  * the shortest possible data retrieval time \(**1 **to **5 **minutes\);
  * a cost of $**0.03 **per GB and $**0.01 **per request.

    You can use any of the following Expedited data retrieval modes:

    * **On-Demand**

      On-Demand requests are similar to [EC2 On-Demand instances](https://aws.amazon.com/ec2/pricing/) and are available most of the time.

    * **Provisioned**

      Provisioned capacity guarantees that your retrieval capacity for Expedited retrievals is available even when demand for such retrievals is very high. Provisioned capacity units allow you to pay a fixed up-front fee to expedite retrievals from Amazon Glacier vaults for a given month.

      When you select this option, all Expedited retrievals will automatically be served via your Provisioned capacity. Each unit of Provisioned capacity costs $**100 **per month and ensures that at least three expedited retrievals can be performed every five minutes with up to **150 **MB/s of retrieval throughput. If you exceed that limit, expect errors on the part of Amazon.

      > See the following document to learn more about this feature: [Provisioned Capacity](https://docs.aws.amazon.com/amazonglacier/latest/dev/downloading-an-archive-two-steps.html#api-downloading-an-archive-two-steps-retrieval-expedited-capacity).

