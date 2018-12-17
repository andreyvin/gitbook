<h2>Backing Up EC2 instances via MBS Web Console</h2>

<p>MBS Web Console features custom Amazon EC2 backup functionality that enables you to back up your EC2 instances to Amazon S3 storage service. The main differentiating factor of our EC2 backup implementation is that it takes Amazon’s native snapshots and builds on them by adding various technical improvements. </p>

<p>Let’s examine the main characteristic of MBS’s EC2 backup. First, by using VSS snapshots, MBS ensures that the resulting backups can be consistently restored as EC2 instances. Second, MBS backs up metadata of an instance to be able to perform item-level restore in the future. That way, by combining EC2 native snapshot functionality and MBS’s add-ons, you can significantly improve the quality and flexibility of your backup and restore routines.</p>

<h3>Creating a Backup Plan</h3>

<p>To get started with MBS EC2 Backup, go to the <b>Remote Management</b> tab, under <b>RMM</b>.</p>
<div class="help_img"> <img style="max-height: 400px;max-width: 750px" src="../contents/images/ec2backup/ec2backup1.png">  </div>

<p>In the list of computers, locate the required EC2 instance and click on its name.</p>
<div class="help_img"> <img style="max-height: 400px;max-width: 750px" src="../contents/images/ec2backup/ec2backup2.png">  </div>
